# Introduction

#### Si vous n'êtes pas familier avec Ansible, je vous conseille de commencer par ce repository : [ansible-react-node](https://github.com/IsoardiMarius/ansible-node-react)

Ce repository contient les sources pour le déploiement avec Ansible d'une app react connecter à un backend nodejs, qui est lui même connecter à une base de donnée mariadb.

#### Un tutoriel est mis à votre disposition, vous serez guidé pas à pas pour déployer l'application sur votre machine virtuelle : [Tutoriel ansible-galaxy](https://picayune-promotion-42d.notion.site/Mac-M1-deployment-ansible-galaxy-with-Debian-11-node-mysql-react-693e5b2ce3aa41378aa3d9d537584998)


## Requirements

- Une machine virtuelle avec un OS Debian 11
- Ansible sur votre machine en locale

## Installation
- Commencer par cloner le repo sur votre machine
- Copier les fichiers inventory et playbook.yml dans le dossier /etc/ansible
- Modifier le fichier inventory avec les informations de votre machine virtuelle
- Modifier le file .env sur le projet (dans le dossier backend) et l'url de l'api sur l'app react (dans le fichier frontend/src/App.tsx)
- Lancer la commande ansible-playbook -i inventory playbook.yml -vvv



```bash
# Clone the repo
git clone https://github.com/IsoardiMarius/ansible-node-react.git

# Move files
mv ansible-node-react/inventory /etc/ansible
mv ansible-node-react/playbook.yml /etc/ansible

# Modifier le file .env sur le projet (dans le dossier backend) et l'url de l'api sur l'app react (dans le fichier frontend/src/App.tsx)

# Modifier le fichier inventory avec les informations de votre machine virtuelle
nano /etc/ansible/inventory

# Run ansible
ansible-playbook -i inventory playbook.yml -vvv
```



