# jmattheis/devops

Stuff that I host.

## Setup Servers

Most of the roles uses pacman as package manager therefore an arch linux system is required.
[archwiki.org Install Guide](https://wiki.archlinux.org/index.php/Installation_guide)

## Usage

| Command                                              | Description                          |
| ---------------------------------------------------- | ------------------------------------ |
| `ansible-playbook playbook.yml`                      | Installs servers                     |
| `ansible-playbook playbook.yml -e type=backup`       | Backups servers to `./backups/`      |
| `ansible-playbook playbook.yml -e type=apply-backup` | Applies the backup from `./backups/` |

## Roles

| Role                                     | Description                                              |
| ---------------------------------------- | -------------------------------------------------------- |
| [common](roles/common)                   | Installs and configures packages like fail2ban, vim, etc |
| [docker](roles/docker)                   | Starts Docker                                            |
| [teamspeak](roles/teamspeak)             | Starts a ts3server and sinusbot                          |
| [gotify](roles/gotify)                   | Starts [gotify/server](https://gotify.net)               |
| [nextcloud](roles/nextcloud)             | Starts [Nextcloud](https://nextcloud.com/)               |
| [nginx-tls-proxy](roles/nginx-tls-proxy) | Starts a nginx proxy and a companion for tls             |
