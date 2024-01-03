# ansible-vault-2
We will be encrypting the secret file using ansible-vaults:
```
ansible-vault encrypt secret
```
View the encrypted secret like so:
```
ansible-vault view secret
```
Create Vault password file may be used to acess the encrypted secret file
```
echo 'myPass' > /home/ansible/vault
```

Execute pre-flight checks
```
ansible-playbook --vault-password-file vault secPage.yml --check
```

Run the playbook passing the password file
```
ansible-playbook --vault-password-file vault secPage.yml
```