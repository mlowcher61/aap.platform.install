# aap.platform.install
Automate that Ansible Automation Platform install

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