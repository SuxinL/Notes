# git rebase

## What

A tool to reapply changes on the top of another commit.

## Purposes

- a clear history
    - makes it linear 
    - groups related changes together
- remove buggy commits

## When

## Where

## How

### Philosophy

- Changes Not Commits: Rebasing commits does NOT mean moving these commits to another place. Only changes made in these commits will be applied. 
- Like Merge: When combining two branches, `rebase` and `merge` are required to have the same final effect (the final snapshot).
 
 ### Behaviors
 
- input(a type of movement): `git rebase --onto <new_base> <upstream> <branch>`
    - what to reapply(start): changes made in `<branch>` but not in `<upstream>`
    - where to reapply(end): `<new_base>`
- output: git reapplies changes in these commits one commit by one commit onto the new base. 