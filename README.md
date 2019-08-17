# ansible-owncloud-docker

Use Ansible to setup ownCloud in Docker.

## Get Started

get a server ready, make sure you can ssh to it:

    ssh ubuntu@HOST_IP

add server to your ansible inventory:

    sudo vim /etc/ansible/hosts

    owncloud ansible_host=HOST_IP ansible_user=ubuntu

edit vars in main.yml:

    vim main.yml
    # modify default vars, change admin username and password, http port, etc.

run ansible:

    ./main.yml -v

access owncloud web interface:

    http://HOST_IP:8080


## What it does

- install docker and doker-compose
- render docker-compose.yml
- install supervisor and render conf for owncloud
- run docker-compose for owncloud with supervisor
