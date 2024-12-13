# EPUB

## what

EPUB, short for Electronic Publication, is an e-book file format. It is an open standard and widely supported by most platforms.

## purposes

- efficiency
    - reflowing for a display
    - TOC
    - multimedia supported

## when

- read from screens of different sizes like pads and phones
- want to adjust font sizes

## where

- usually on small displays

## how

### Content

- philosophy
    - It uses the general web technology for display
- structure
    - XHTML for content of books
    - CSS/JS for styling and presentation
    - multimedia
        - images
        - videos

### Arrangement

- philosophy
    - to manage and navigate efficiently
    - XML files for the meta info
- structure: contains 2 XML files
    - content.opf
        - metadata: contains basic info about a book
            - id
            - title
            - language
        - manifest: lists all files contained in the package
        - spine: organizes all the XHTML content files
            - linear reading order
            - ref to the TOC file
    - toc.ncf

### Packaging

- philosophy
    - all related files are bundles in a zip package
    - a mimetype file for identifying the e-book format as EPUB
    - container.xml referring to the entrance file of the book - content.opf  