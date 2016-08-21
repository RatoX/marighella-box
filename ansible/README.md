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


2) Install the tools

```
ansible-playbook -i dev tools.yml --vault-password-file=~/.ssh/vault_password_file
```
3) Test!

4) Hardning it!
```
ansible-playbook -i dev security.yml --vault-password-file=~/.ssh/vault_password_file
```

