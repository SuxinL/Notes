# 189 cloud

## what

A cloud platform provided by China Telecom.

## purposes

- efficiency
    - sharing
- security
    - backup

## when

- we have important resources

## where

- cross-platform
    - web
    - phones

## how

- auto backup
    - purposes
        - to backup resources in certain folders **immediately** for later process.
    - how
        - interfaces
            - philosophy
                - folder-binding: any new data in a local folder will be uploaded into its binding folder in the cloud.
                    ```mermaid
                    flowchart
                    M(manager)
                    subgraph L [local]
                        F1(folder 1)
                    end
                    subgraph C [cloud]
                        F2(folder 2)
                    end

                    M -->|get| F1
                    M -->|put| F2
                    F1 -.-|binding| F2
                    ```
            - turning
                - get
                - set
                    - enable/disable
                    - binding path
                    - conditions
                        - network types
                        - battery threshold
- manual management
    - purposes
        - filter & organize data
            - photo albums
            - docs
    - how
        - file management
            - folder/file
                - philosophy
                    - real storage: This structure represents how data is stored in the cloud.
            - family space
                - philosophy
                    - 2 storage parts: Each user has its own personal and family storages.
                    - switch to the family storage of another user: when in the family storage of another user, all operations take effects on his family storage.
        - photo management
            - philosophy
                - photo albums are views of storage: 
                    - a photo can appear in multiple albums.
                    - deleting a photo from albums will NOT delete it from the storage.
                - person and family photo management separated
                    - personal albums can only show photos in the personal storage
                    - family albums can only show photos in the family storage
                    - local photos added into an album will be uploaded into the corresponding storage.
                - 3 level
                    - album management
                        - photo management
                            - photo editing 