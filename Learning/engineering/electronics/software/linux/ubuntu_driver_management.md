# ubuntu driver management

## what

A mechanism to manage all device drivers.

## purposes

To easily manage all drivers **at one place**.

## when

- trouble shooting when a device is inaccessible.
- update drivers
- check current configuration.

## where

- Ubuntu

## how

### philosophy

- package: Driver files are treated as modules in Ubuntu, which are a type of packages.
- kernel-builtin: Unlike Windows where we need to install drivers by ourselves, Linux kernels include most of drivers already, then makes a system usable out of box. We need to install drivers if we want to use **propriety** ones like Nvidia GPU drivers.  

### types

- general way: **APT**
- driver oriented: **these tools only display available propriety drivers**
    - CLI: `ubuntu-drivers`
    - GUI: Additional Drivers

### behaviors

- get
    - in use
    - installed 
    - available
- set
    - install
        - from standard repositories
        - from another repository
        - using official installers 
    - remove
    - switch

