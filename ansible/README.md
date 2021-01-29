# Ansible

### Настройка
1. В файл `.vault_pass` добавить пароль `root` для ansible vault.
1. Для корректной работы ansible лучше использовать virtualenv:
    ```shell script
    virtualenv -p /usr/local/bin/python3 ~/.local
    . ~/.local/bin/activate
    ```
1. Установить необходимые зависимости:
    ```shell script
    pip install -r requirements.txt
    ```
1. Установить дополнительные коллекции ansible:
    ```shell script
    ansible-galaxy install -r galaxy.yml -p roles
    ```
   
### Запуск playbook
```shell script
ansible-playbook -i inventories/local/static.yml --vault-password-file=.vault_pass mongodb.yml -v
```