# MongoDB Master-Slave replication

1. Add vault password to `.vault_pass`.
2. Run command:
```bash
ansible-playbook -i inventories/static.ini --vault-password-file=.vault_pass mongo.yml
```