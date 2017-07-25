# Ansible Playbook for deploying Polymer projects


Deploy your Polymer 2.0 project to your server using NGINX as WebServer.

## Actions

  1. Install NGINX
  2. Install and Configure Certbot for installing an SSL Certificate, by
     Let's encrypt.
  3. Copy your project build/default files in the server's
     /apps/your_project_name directory.

## Configuration

Change your project details in **env/vars/base.yml** and
**env_vars/develop.yml**.

The file inventory is your servers inventory, put your server IP below
**[webservers]**.

Then run it:

```
ansible-playbook site.yml -i inventory
```

