# Android App Use Limit

## what

- a system utility that limits use time of installed apps. When the use time reaches its limit, an app will be blocked until the next day.  

## purposes

- efficiency
    - productivity: avoid distractions
        - working
        - sleeping

## when

- we do not want waste time on distracting apps.

## where

- android

## how

- philosophy
    - **APP-LEVEL**: this utility works on app level, which means if an app is blocked, all its functionalities are blocked. It can not be used to block a module of an app like only blocking some sites for a browser.
    - **ID_TRACKING**: It records the id of an app, which makes the blocking work even after the app is deleted and reinstalled.
- schedule manager
    - attributes
        - rule
            - password
        - state: on/off
    - schedule list
- schedule
    - state: on/off
    - app
    - applied days
    - limit each day