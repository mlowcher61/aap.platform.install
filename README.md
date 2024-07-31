# Ansible Automation Platform Installation
Automate that Ansible Automation Platform install

**Build an infrastructure that meets the requirements**

[Red Hat Ansible Automation Platform 2.4](https://access.redhat.com/management/api "Red Hat Ansible Automation Platform 2.4")

**Legacy Ansible Platform install command line with vaulted creds**
```
ansible-playbook -i inventory ansible.containerized_installer.install -e@ames_vault.yml --vault-password-file ~/.ssh/secret
ansible-playbook -i inventory ansible.containerized_installer.install -e@ames_vault.yml --ask-vault-pass
```
**Containerized Ansible Platform install command line with vaulted creds**
```
./setup.sh -e@ames_vault.yml -- --vault-password-file ~/.ssh/secret
./setup.sh -e@ames_vault.yml -- --ask-vault-pass

```