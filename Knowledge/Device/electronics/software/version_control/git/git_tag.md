# git tag

## What

a tool to handle tags in git.

## Purposes

- tags to mark important points.

## When

- when we want to refer to something like a specific version of a file or the whole project later.

## Where

git repositories

## How

### behaviors

- get
    - to list all tags
        - input: `git tag [-l]`
        - output:  a list of tag names
    - to show the content of a tag
        - input: `git show <tag_name>`
        - output: the content of tag if it is an annotated tag, and content of the object that it refers to.
    - to show the id of the object that a tag refers to.
        - input: `git show-ref --tags --dereference <tag_name>`
        - output: 
            - one line for the tag, and one line for the object
                - for each line, the hash and name.

- set
    - to delete a tag
        - input: `git tag -d <tagname>`
    - to push tags into a remote rep
        - input: `git push --tags`

### Structure

There are 2 types of tags - lightweight and annotated ones.

#### lightweight tags

- what: a reference to a git object.
- purpose: a private or temporary label.
- how
    - behaviors
        - set
            - create: `git tag <tagname> <object>`
       
#### annotated tags

- what: an object containing a ref to a git object.
- purpose: for release.
- how
    - structure
        - tagger info
            - name
            - e-mail
        - a creation date
        - a tagging message
        - a ref to the tagged object.
    - behaviors
        - set
            - create: `git tag -a <tagname> <object>`