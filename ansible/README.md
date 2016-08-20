# Problemas:

`SSH Error: data could not be sent to the remote host


export ANSIBLE_SCP_IF_SSH=y


#To run on DEV
1) Create the user first

ansible-playbook -i dev user.yml --vault-password-file=~/.ssh/vault_password_file --private-key=~/.ssh/id_rsa

2) Install the app

3) Test!

4) Hardning it!

