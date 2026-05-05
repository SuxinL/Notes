# powertop

## what

a tool to display power usages of the system and its components, and to change some power settings.

## purposes

- to save power and extend battery life.

## when

- check current power usage situation
- find and handle power-consuming apps and devices.

## where

- linux

## how

### structure

- overview
    - system power usage
    - a list of **apps** in a power consumption descending order. 
        - each list item: represents a process
            - usage: represents how much time of the cpu is used for the process.
- cpu
- devices 
    - a list of **devices** in a power consumption descending order.
        - each list item: represents a hardware device.
            - usage: represents how many percent of time a device is active.
- turnable
    - a list of user turnable power settings for devices
        - each list item: the setting for a device
            - status: the status of the current setting in terms of power saving
            - description: the meaning of the setting
- wake-up

### behaviors

- get    
    `tab` and `shift+tab` to switch views.
- set
    - click `return` for any turnable item: switch the values of the setting.
        - `on`: makes the device always on.
        - `auto`: enables [auto suspend](https://www.kernel.org/doc/html/v4.16/driver-api/usb/power-management.html).