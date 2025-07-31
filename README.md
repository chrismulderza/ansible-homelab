# ansible-homelab

My Ansible project that sets up and maintains my HomeLab environment.

## Usage

All playbooks should be executed as part of the collection. Playbooks are
created in `collections/ansible_collections/bitbuild/homelab/playbooks`.

Example execution:

```bash
ansible-playbook bitbuild.homelab.ping
```

## Project layout

### Collection

Created the collection with:

```bash
ansible-galaxy collection init --init-path collections/ansible_collections bitbuild.homelab
```
