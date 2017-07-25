# Ansible Playbook for deploying Polymer 2.0 projects


Deploy your Polymer 2.0 project to your server using NGINX as
WebServer with HTTPS.

## Actions

  1. Install and configure NGINX to serve your domain and a Polymer
     Single Page Application (all routes are served by index.html).
  2. Install and Configure Certbot for installing an SSL Certificate, by
     Let's encrypt.
  3. Copy your project build/default files in the server's
     /apps/your_project_name directory, to serve it.

## Pre-requisites

In order to configure and use Let's Encrypt certificates, you need a DNS
record pointing to your server with the domain you're intending to use
for the deploy.

This project is intended to deploy a SPA, so all routes are rewritten
and served by index.html. For example, if your application was built
with the Polymer Starter Kit, this project will help you deploy it.

## Configuration

Change your project details in **env/vars/base.yml** and
**env_vars/develop.yml**.

The file inventory is the ansible's inventory file, put there your server IP below
**[webservers]**.

Then run it:

```
ansible-playbook site.yml -i inventory
```

