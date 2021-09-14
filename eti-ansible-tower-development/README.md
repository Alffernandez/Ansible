# eti-ansible-tower

## Prerequisites

Install the Ansible Tower collection (this will be installed in your home directory). This isn't required when the playbook is being run from a Template in Tower.

```bash
ansible-galaxy collection install collections/ansible-tower-3.7.0.tar.gz 
ansible-galaxy collection install --force collections/ansible-tower-3.8.3.tar.gz 
```

## Vault

Use UNIX Vault password

```bash
ansible-vault edit vars/vault.yml 
```

## Usage

- Deploy everything to dev

```bash
ansible-playbook -i inventory -l dev tower_config.yml --vault-password-file=/etc/vault/.vaultpw
```

- Deploy only templates to prod

```bash
ansible-playbook -i inventory tower_config.yml --vault-password-file=/etc/vault/.vaultpw -l dev -t templates 
```
