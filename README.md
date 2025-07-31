# ansible-homelab

My Ansible project that sets up and maintains my HomeLab environment.

## Usage

All playbooks should be executed as part of the collection. Playbooks are
created in `collections/ansible_collections/bitbuild/homelab/playbooks`.

Example execution:

```bash
ansible-playbook bitbuild.homelab.ping
```

## Whats included

### Playbooks

#### `bitbuild.homelab.ping`

Simple pinger playbook to check connectivity to hosts.

#### `bitbuild.homelab.bootstrap_ansible`

A playbook to bootstrap a new host to be managed by Ansible. You will need to
supply a user that is able to `ssh` into the host. The playbook only operates
on the `unmanaged` host group in the [inventory](inventory/hosts.yml).

### Roles

## Project layout

### Collection

Created the collection with:

```bash
ansible-galaxy collection init --init-path collections/ansible_collections bitbuild.homelab
```

#### Roles

Add a new role to the `collections/ansible_collections/bitbuild/homelab/roles`
path.

Create a role with:

```bash
ansible-galaxy role init packages
```

Update the metadata in `meta/main.yml`
