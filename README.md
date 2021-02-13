# ansible-pull

Pull configurations for setting up machine form git. You need password file to run this repo`

## Requirements

- git
- ansible
- ansible vault password
- git repo access

## How to run

Run ansible-pull command on new machine using below command once.

```
sudo ansible-pull git-repo-path --vault-password-file 'passwordfile'
```

It will automatically setup cron job to run ansible-pull every 30 minutes.

- code to import git clone

```
git clone https://${gittoken}:x-oauth-basic@github.com/belibug/ansible-pull.git
```

## Pending

- figure out basic accounts setup (thinking bootstrap)
