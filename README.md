# Proxmox Playbook

This repository manages hosts on a Proxmox Cluster, as well as any guest VMs and LXCs.

### Installing Ansible

There are [official Ansible steps](https://docs.ansible.com/ansible/latest/installation_guide/index.html) to install the Ansible CLI on your local machine (or any other machine) you will be using as a controller node.

### Running the Playbook

1. Make sure dependencies are installed:
```
ansible-galaxy install -r requirements.yml
```

2. Run the entire playbook:
```
ansible-playbook playbook.yml
```

3. Alternatively, you can use tags:
```
# run just the users tasks
ansible-playbook -t users playbook.yml

# run everything except the users provisioning
ansible-playbook --skip-tags users playbook.yml

# update mergerfs
ansible-playbook -t mergerfs playbook.yml
```
