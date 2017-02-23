ANSIBLE_SCP_IF_SSH=y
ENVIRONMENT=dev

new-one:
	ansible-playbook -i $(ENVIRONMENT) user.yml --vault-password-file=~/.ssh/vault_password_file --ask-sudo-pass --user=root --ask-pass

tools:
	ansible-playbook -i $(ENVIRONMENT) tools.yml --vault-password-file=~/.ssh/vault_password_file

nginx:
	ansible-playbook -i $(ENVIRONMENT) nginx.yml --vault-password-file=~/.ssh/vault_password_file

security:
	ansible-playbook -i $(ENVIRONMENT) security.yml --vault-password-file=~/.ssh/vault_password_file

auth:
	ansible-playbook -i $(ENVIRONMENT) applications/auth.yml --vault-password-file=~/.ssh/vault_password_file
