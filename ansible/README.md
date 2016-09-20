# Problemas:

SSH Error: data could not be sent to the remote host


export ANSIBLE_SCP_IF_SSH=y


#To run ( first time to create the user )
1) Create the user first

DEV
```
ansible-playbook -i dev user.yml --vault-password-file=~/.ssh/vault_password_file
```
stage
```
ansible-playbook -i stage user.yml --vault-password-file=~/.ssh/vault_password_file --ask-sudo-pass --user=root --ask-pass
```

##Troubleshooting
Adding this flag to use the private key
```
--private-key=~/.ssh/id_rsa
```


2) Order to install

- user.yml  "Add ratox user
- tools.yml "We need tools
- application/backend.yml "Install backend project
- nginx.yml "Setup a nginx server
- security.yml "Hardening the server
