# Ansible Automation Platform Installation
Automate that Ansible Automation Platform install

**Build an infrastructure that meets the requirements**

[Red Hat Ansible Automation Platform 2.4](https://docs.redhat.com/en/documentation/red_hat_ansible_automation_platform/2.4/ "Red Hat Ansible Automation Platform 2.4")

**Create vaults for your secrets using ansible-vault**
- [Password to unlock your vault](https://github.com/ericcames/aap.platform.install/blob/main/roles/ansible_platform_install/files/secret_example.yml "Password to unlock your vault")
- [Vault that will be used by the inventory file](https://github.com/ericcames/aap.platform.install/blob/main/roles/ansible_platform_install/files/vault_example.yml "Vault that will be used by the inventory file")
- [Update your role default variables](https://github.com/ericcames/aap.platform.install/blob/main/roles/ansible_platform_install/README.md "Update your role default variables")

**Legacy Ansible Platform install command line with vaulted creds**
```
./setup.sh -e@ames_vault.yml -- --vault-password-file ~/.ssh/secret
./setup.sh -e@ames_vault.yml -- --ask-vault-pass
```
**Containerized Ansible Platform install command line with vaulted creds**
```
ansible-playbook -i inventory ansible.containerized_installer.install -e@ames_vault.yml --vault-password-file ~/.ssh/secret
ansible-playbook -i inventory ansible.containerized_installer.install -e@ames_vault.yml --ask-vault-pass

```