# Infrastructure for production

This repo goal is to simplify updates on my virtual servers (currently, aws ec2)
There are few subdomains which lead to my virtual server and nginx-proxy-manager who helps with proxying them to different docker-containers


## Requirements
All the roles work with this ansible setup
Don't forget about having vault password file :)
```bash
$ ansible --version
ansible [core 2.14.3]
  ...
  python version = 3.11.2
  jinja version = 3.1.2
  libyaml = True

$ ansible-vault --version
ansible-vault [core 2.14.3]
  python version = 3.11.2 
  jinja version = 3.1.2
  libyaml = True

```

## Usage
There are 5 playbooks.

####playbook.yml 
for configuring instance
```bash
 ansible-playbook playbook.yml --vault-password-file PASSWORD_FILE
```

####update-( personal-site | sport-bot | sport-system | svelte-portfolio).yml
for updating specific subdomain and its data
```bash
 ansible-playbook PLAYBOOK_FILE --vault-password-file PASSWORD_FILE
```
