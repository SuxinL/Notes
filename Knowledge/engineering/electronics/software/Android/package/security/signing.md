# APK Signing

- sys
    - install
    - update
- install
    - main points
        - what
            - During installation, the signature of an package is required to be verified.
        - purposes
            - security
                - authenticity
                - integrity
    - body
        - signing schemes
            - v1
            - v2+
        - management
            - basic
                - get
                    - summary
                        - comparison
                            | Aspect | v1 | v2+ |
                            | --- | --- | --- |
                            | Protected range | parts | whole file |
                            | Verification Speed | low | fast |
            - interaction
                - compatibility
                    - an application is firstly signed with v1, then v2+. 
- update
    - signature verification
    - additional checks
        - id match
        - signing certificate match
        - higher version
- signing certificate match
    - main points
        - what
            - The signing certificate of the update must be the same as the signing certificate of the installed app
        - purposes
            - security
                - FRAUD: avoid installing an app with the same id but from another developer.