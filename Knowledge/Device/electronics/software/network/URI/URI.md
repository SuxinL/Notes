# URI

## what

a Uniform Resource Identifier is a sequence of characters to identify a resource.

## purposes

- efficiency
    - uniform
        - different systems can understand the same URL.
        - different types of URLs can be used in a context.
    - global transcription
        - Characters used can be typed from keyboards.
    - structure

## when

- to search for a resource

## where

- In network

## how

### characters

Allowed characters in URIs are a subset of those in ASCII.
- character encoding

    to store or transmit URIs, chosen by the scheme.
- reserved

    used as delimiters to separate components.
    - general

        generally used delimiters
    - sub

        may or may not used by a scheme as delimiters.
- unreserved

    used as component data.
    - ALPHABET
    - DIGIT
    - `~`, `-`, `_`, `.`
- percent encoding
    - purposes
        - to use characters out of the allowed set.
        - to use reserved ones as component data.
    - how
        1. for a char out of the allowed set, find its code point in UTF-8
        2. represent each byte of the code point with `#` followed by the two digits of the hex value of the byte. 

### syntax