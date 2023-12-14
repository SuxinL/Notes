# SSH

## what

ssh is a protocol for a client to access a remote server securely. The client can login to and run commands on the server.

## purposes

- security

## when

## where

## how

### Authentication

- philosophy
    - encryption

        the channel is encrypted since before the authentication process.
        
    - authentication
    
        both-side authentications are requested.
        - client
            - host
            - public-key
        - server
            - **Trust On First Use**: The end user checks the public key of the server manually before the first time of communication. 
                - If it is authentic, the client stores it for later automatic checking.
                - less overhead than certificates but manual work needed.

- structure
    ```mermaid
    flowchart 
        subgraph client
            ssh
            ssh-agent
            keys
            config 

            ssh-agent --> keys
            ssh --> ssh-agent
            ssh --> config
            ssh --> known_hosts
        end
        subgraph server
            sshd --> authorized_keys
        end
        ssh -.- sshd
    ```
    - client
        - ssh: the ssh client communicating with remote servers.
        - ssh-agent: holds identities including private keys in memory.
        - known_hosts: a file containing lists of known hosts.
        - config: git config files. **A Mapping from a host nickname to a combination of host, user and identity enables us to login to a server with different accounts by only specifying the host nickname.**

#### ssh agent

SSH enables us to encrypt identities including private keys with passphrases which however require manual typing in. To avoid this manual operation for each access, a ssh agent can be run to hold unencrypted identities in memory for a user session.