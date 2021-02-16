# ansible-pull

Pull configurations for setting up machine form git. You need password file to run this repo`

## Requirements

Create below requirements with bootstrap shell script

- git
- ansible
- ansible vault password
- git repo access

## How to run

Run ansible-pull command on new machine using below command once.

```
sudo ansible-pull git@github.com:belibug/ansible-pull.git --key-file somefile --vault-id bug@prompt --accept-host-key
```
You can use api-token instead of key for first run

It will automatically setup cron job to run ansible-pull every 30 minutes.

- code to import git clone

```
git clone https://${gittoken}:x-oauth-basic@github.com/belibug/ansible-pull.git
```

## Pending

- setup bug user
- add authenticated users to ssh list
- set dot files sync
- set failed alert
- reconfigure to use vault-id instead of password file for first run

## setup Ansible Play for scheduled tasks

- udpate and upgrade repos
- security stuff
	- check and clean users
	- check backup
- perform git pull
