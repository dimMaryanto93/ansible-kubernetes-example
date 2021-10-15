## Ansible - User Guide

Persiapan yang harus di lalukan, diantaranya

1. Create new user on your server, Recomend using **very-very Strong Password** or using password generator.  

    ```bash
    adduser <username>
    ```

2. Granted to sudoers with NOPASSWD, using `visudo`
    ```ini
    username    ALL=(ALL) NOPASSWD:ALL
    ```

3. Authenticate with private-key for login ssh, generate ssh key on your local machine then use `ssh-copy-id user@your-ip-server` to copy public key to your server.

### Using Ansible Playbooks

This is ansible for installing Docker CE, currently support for 

- CentOS 7
- Ubuntu 20.4

This page show you step-step installing docker using Ansible. First install requirement using command:

```bash
ansible-galaxy collection install -r requirements.yaml
```
