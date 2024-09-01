# sysfs

## what

sysfs is virtual file system containing information of kernel objects representing state and structure of devices and drivers.

## purposes

- efficiency
    - It provides an **unified** interface for user applications to access all devices.

## when

- get
    - to check the structure of a system or details of a device including id info, the used driver, power settings and current status.
- set
    - to configure a device

## where

- since Linux 2.6

## how

### structure

It provides different views. 
- devices: this view organizes all devices in the physical layout.
    - pci
        - usb
            - a usb keyboard
                - id
                - driver
                - firmware
                - power
- bus: this view organizes devices based on the types of buses that they are attached to.
    - for each type of bus there is a dir
        - devices
        - drivers 
- class: this view organizes devices based on devices' functionalities.
    - for a functionality there is a device class dir
        - for each device registered into this device class, there is a device object.
            - state
            - physical device

### behaviors

- get
    - file navigation commands
    - summary tools
        - [`lshw`](lshw.md)
        - `lspci`
        - `lsusb`