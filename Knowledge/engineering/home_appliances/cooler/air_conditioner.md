# Air Conditioner

## what

An device which cools indoor air and removes water vapor. 

## purposes

- efficiency
    - comfort
- security
    - prevent molds

## when

- hot days
- wet days

## where

- indoor
    - home
    - office
    - factory

## how

### interface

- temperature
- duration
- intensity     
- modes
    - cool
    - heat
    - dry: firstly cool the space to condense and remove water vapor, then heat the space to restore the temp.
    - fan: only run the fan to circulate indoor air for mild cooling.
    - sleep: increase the temp gradually to offset body heat loss overnight to help maintain sleep.

### structure

- principles
    - [vapor compression refrigeration](https://en.wikipedia.org/wiki/Vapor-compression_refrigeration): A refrigerant is used as a medium to transfer heat from an enclosed space to outside.
- layout
    ```mermaid
    flowchart 
        E[Evaporator]
        CP[Compressor]
        CD[Condensor]
        EV[Expansion Valve]

        E -->|saturated vapor| CP -->|superheated vapor| CD -->|saturated liquid| EV -->|mix| E
    ```
    - Evaporator
        - to absorb heat from the target enclosed space to the refrigerant.
    - Compressor
        - to compress the refrigerant to a superheated vapor whose temperature is higher than ambient air of the condensor.
        - to power the flow.
    - Condensor
        - to reject heat from the refrigerant into ambient air.
    - Expansion Valve
        - to lower the temperature of the refrigerant further.

### types
- standalone
    - window
    - wall
    - portable
- split
    - center ducted
    - mini split

| Aspect| Standalone | Split |
| --- | --- | --- |
| definition | a packaged system | split as two parts of an indoor unit containing the evaporator and an outdoor unit containing the compressor, condensor and expansion valve. Two parts are connected by pipes. |
| efficiency | low | high |
| noise | high | low as the noisy compressor is outdoor |
| price | low | high |
| installation | easy | hard |