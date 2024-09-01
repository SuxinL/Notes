# Ubuntu Power Management

## what

a practice of managing power usage by suspending the whole system or parts of the system.

## purpose

- to save power and extend a battery life.
  
## when 

- The batteries are expensive.
- Battery capacities are small.

## where

- linux

## how

### system suspend

- what: suspends the CPU and most of components.
- when: not using the laptop but wanting to preserve the state.
- how
    - suspend
    - hibernate 

    To keep the state of system when not using it and restore it later, there are multiple modes for this functionality.
    
    | Aspect | lock | suspend | hibernate |
    | --- | --- | --- | --- |
    | What | locks the screen, and requires authentication | 1. stops programs running 2. stores current state in MEM 3. supports MEM with minimal power 4. cuts off power to other devices | 1. store current state to disks 2. power off the system |
    | Purposes | Security | Saving power | Saving power |
    | When | 1. leave for a short time 2. leave for a while, but there are programs needing to be running. | want to keep the current state but save power | when this mode is enabled. |
    | Power consumption | High, only the screen is locked. | Low, only supporting MEM | No, the system is totally off. |
    | Requirements | No | No | 1. swap area 2. config |
    | Power Button Light Status | on | shining | off |

### dynamic suspend[^1]

- what: suspends a device while the system remains running. **The dynamic aspect is that whether to suspend or resume a device depends on its runtime usage. If it has not been used for a while, it can be suspended. Likewise, if it is needed later on, it will be resumed.**
- when: 
    - **happens during run-time**. There are methods to turn off a device completely including one through BIOS.
- how
    - philosophy
        - In linux, for system stability, only the kernel can decide to suspend an individual device, while programs or end-users cannot directly ask to do so. In general, the kernel will suspend a device when it has been idle for a specific duration. 
    - structure
        ```mermaid
        flowchart LR
            subgraph running
                B(busy)
                I(idle)
            end
            S(suspended)

            B --> I
            I --> B
            I --> |auto suspend|S
            running --> |system suspend|S
            S --> |auto resume| running
            S --> |external resume| running
        ```
        - idle: A device is idle whenever the kernel thinks that it is not busy doing something.
        - suspended: When a device is suspended, it is in a nonfunctioning low-power state; it might even be turned off completely.
    - events
        - internal: those triggered inside the laptop. 
            - auto suspend: Auto suspend is just dynamic suspend decided by the kernel.
            - auto resume: The kernel automatically resumes a device when a program needs to use it. 
        - external: those triggered by external agents like end-users.
            - system suspend: when a user asks to suspend the whole system, the device is forced to suspend.
            - external resume
                - system resume
                - manual dynamic resume: A user asks a device to resume like through sysfs power config.
                - remote wakeup

                    The device resumes itself in response to some external events. For instance, a suspended keyboard could resume when a key is pressed.

                    Making a suspended device in a low-power state rather than turned off cracks this **chicken-egg problem**. The device can resume itself by 
                    - itself
                    - asking the kernel to resume it
                    - telling the entire computer to resume
    - user interfaces for config

        In sysfs, there is a `power` dir for each device traced from the bus view like `/sys/bus/pci/devices/0000:00:1f.6/power`. Under this `power` dir are 3 attribute files to config auto-suspend and remote-wake.
        - `control`
            - `on`: always running
            - `auto`: auto-suspend enabled.
        - `autosuspend_delay_ms`: the delay time duration in ms before a device should be auto suspended.
        - `wakeup`
            - empty: remote wakeup is not supported. 
            - `disabled` 
            - `enabled`   

        > NOTICE: sysfs provides an interface to access **kernel objects which are in the memory**. To make this config persist, edit `/etc/sysfs.conf` provided by `sysfsutils`.

[^1]: https://www.kernel.org/doc/html/v4.16/driver-api/usb/power-management.html