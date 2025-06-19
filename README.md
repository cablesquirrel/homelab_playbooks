# Homelab Playbooks

Author: Eric Hansen <ericzone.admin@gmail.com>

## EE Build

An execution environment is included in the project to be able to run on modern platforms such as AWX. Ansible-Navigator
is configured to run the playbook using this environment.

```bash
cd ee
ansible-builder build --tag ghcr.io/USERNAME/homelab_playbooks:latest --container-runtime docker

export CR_PAT="YOUR_PAT_HERE"
echo $CR_PAT | docker login ghcr.io -u USERNAME --password-stdin

docker push ghcr.io/USERNAME/homelab_playbooks:latest
```
