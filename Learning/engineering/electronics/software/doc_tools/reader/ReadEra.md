# ReadEra

## what

An app to read e-books.

## purposes

- efficiency
    - supporting a lot of file formats
    - book management in the device
    - no ads

## when

- check electronic documents.

## where 

- mainly on phone.

## how

### book management

- philosophy
    - VIEW
        - It enables us to see books from different views which can contain the same book.
        - Deleting a book from views will NOT delete it from device storage.
- interface
    - service
        - get
            - views
                - reading status
                    - in reading
                    - new books
                    - have read
                - favorites
                - collections
                - formats
                - authors
            - scanning: slide down a finger at the top of a view
        - set
            - add to / remove from favorites 
    - tool tuning
        - status signals
        - config
            - scanning
                - scope
                - file types
                - auto scan
            - customized collections

### reading

- philosophy
    - APP METADATA: The information about the status(current page, bookmarks, notes and quotes) of a document is stored as app metadata and NOT written back to the doc.
- interface
    - service
        - get
            - metadata
                - title
                - author
                - language
                - file size
                - percent
            - pages
                - the current page: read
                - adjacent pages: slide
                - page with a specific page number:
                    - slide progress bar
                    - type page number
            - navigation
                - chapters: check TOC
                - bookmarks
                - quotes
            - text handling
                - quote
                - translation
                - dictionary
                - web search  
        - set
    - tool tuning
        - status signals
        - config
            - presentation
                - font
                    - type
                    - size
                    - thickness
                - page
                    - margin
                    - line spacing
                    - orientation
                    - color mode: press the left upper conner to switch
                    - brightness
                        - manual: slide the brightness bar
                        - auto: toggle the A icon
            - text handling app binding
            - operation modes
                - flipping pages