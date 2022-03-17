# Estudos Ansible

Este é um repositório para estudos de automação com a ferramenta Ansible.

## Deploy de aplicação Django

### Requisitos

- Utilizar servidor debian-like
- Adicionar uma chave de deploy no github
- Adicionar o arquivo **vault.yaml** em host_vars/django-host com as seguintes variáveis definidas:
	- vault_database_password
	- vault_project_git_url
	- vault_nginx_server_name

### Run

	ansible-playbook --ask-vault-password -i inventory/hosts.yaml deploy_application.yaml