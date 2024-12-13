# Git

## what

Git is a distributed version control system.

## purposes

- efficiency
    - version management: Git manages versions in a dir `.git` automatically, and avoids side effects on workspace. Users can switch versions via easy interfaces with Git.
    - local: No network is needed. The local repository contains all data needed to do version control work except synchronization.
    - collaboration: Git provides functionalities to communicate with remote servers.
- security
    - distributed design: avoids a single point of failure.
    - backup: The remote repository can also act as a backup. 

## when

- history management for later reference.
- collaboration

## where

- cross-platform
- for any long-term project.

## how

### local

#### commits

- philosophy
    - snapshot not diff: Git stores a snapshot of a project for a commit, then the history is a series of snapshots not patches.
        - retrieving a state of the project is instant, rather than by adding patches from the initial state.
- structure
    ```mermaid
    flowchart RL
        B(master) --> C3(commit 3) --> C2(commit 2) --> C1(commit 1)
    ```
- behaviors
    - get
        - `git log`: displays commits history.
        - `git show`: show various types of objects.
        - `git cat-file`: displays objects in the repository.
        - `git ls-tree`: displays the tree structure represented by an object in the repository
    - set 
        - `git reset [--soft | --hard] <commit>`: resets a branch head to a commit.
        - `git reset <tree-ish> -- <pathspec>`: reset **the index** entries for all paths matched to their state at `<tree-ish>`.
  
#### 3-tree

- philosophy
    - Copy not move: Moving a file from a place to another place here means copying and pasting the file to override the one in the destination. 
- structure
    ```mermaid
    flowchart LR
        W(working tree)
        I(index)
        C(commit)

        W -->|add| I --> |commit| C
        C -->|restore --cached| I -->|restore| W
        C -->|reset| I
        C -->|checkout| I 
        C -->|checkout| W
    ```
    - the working tree: the workspace that a user works on.
    - the index: the pending snapshot preparing for the next commit.
    - the commit: the current commit.
- behaviors
    - get
        - `git status`: displays paths having differences between HEAD and the index or between the index and the working tree.
        - `git diff`: displays different lines of files.
        - `git ls-files`: displays the content of the index and the working tree. 
    - set
        - `git add`: adds a path to the index, which overrides the version in the index with the one in the working tree.
        - `git restore`: restore a path in the working tree, which overrides the version in the working tree with the one in the index, therefore undo changes in the working tree.
            - `git restore --cached`: restore a path in the index with the version in the HEAD, which undoes a previous `git add`.
        - `git commit`: snapshots the index and stores a commit in the repository
        - `git rm --cached`: removes a path from the index to untrack it.

#### branches

- philosophy
    - branches are refs: In git, a branch is a just reference pointing to a commit.
        - It is cheap to create a new branch. Only a new ref is created and no real branch copying is needed.
- structure
    ```mermaid
    flowchart RL
        HEAD --> master --> C2 --> C1
        issue --> C3 --> C2
        fix --> C4 --> C2
    ```
    - branch: a ref to a commit
    - HEAD: a ref to one of branches, representing the active branch.
- behaviors
    - get
        - `git branch`: list branches
    - set
        - create `git branch <branch_name>`
        - delete `git branch -d <branch_name>`
        - rename `git branch -m <branch_name>`
        - combine
            - `git merge`: replays changes since diverged on the top of another branch
                - fast-forward
                - three-way merge
            - [`git rebase`](git_rebase.md): replays commits one by one on the top of another commit.
        - switch `git checkout`: sets HEAD referring to another branch, and updates the index and working tree.     

##### merge V.S rebase

`rebase` can achieve the same final output as `merge`, but with additional functionalities by specifying which commits to replay to which commit.
- a clear history
    - makes it linear 
    - groups related commits together
- remove buggy commits

### remote

- philosophy
    - 2-level specification
        - repository: where to sync
        - ref: what to sync
- structure
    ```mermaid
    flowchart 
        subgraph LOCAL
            B(local branch)
            RT(remote-tracking branch)
        end
        subgraph REMOTE_REPOSITORY
            R(remote branch) 
        end

        RT -->|merge| B
        R -->|fetch| RT
        B -->|track| RT
        B --> |push| R
    ```
    - remote branch: a branch in the remote repository.
    - remote-tracking branch: for each involved remote branch, there is local remote-tracking branch reflecting its state at the last time of synchronization. Each time of `fetch` git automatically updates it, and users cannot modify it.
    - local branch: a normal local branch for a user to operate. If a local branch is tracking a remote-tracking branch, it can be called a tracking branch. 
- behaviors
    - get
        - `git remote`: lists remote repositories.
    - set
        - `git remote add`: adds remote repos.
        - `git branch -u <upstream> <branch_name>`: makes a local branch track a remote-tracking branch for
            - default merge branch in `git pull`
            - tracking status
        - `git fetch`: downloads refs and objects from remote, and update remote-tracking branches.
        - `git merge`: merges a remote-tracking branch into the current branch
        - `git pull`: fetches, then merges
        - `git push`: pushes local updates to remote.

### auxiliary

- git [tags](./git_tag.md): to mark important points for later references.