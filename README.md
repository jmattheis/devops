# jmattheis/devops

Stuff that I host.

## Setup Servers

Most of the roles uses pacman as package manager therefore an arch linux system is required.
[archwiki.org Install Guide](https://wiki.archlinux.org/index.php/Installation_guide)

## Playbooks

### `install.yml`

Installs and starts services.

```bash
$ ansible-playbook install.yml
```

### `backup.yml`

Downloads all relevent data for the installed services to `./backups`.

```bash
$ ansible-playbook backup.yml
```

### `apply-backup.yml`

Applies the backup from `./backups`.

```bash
$ ansible-playbook apply-backup.yml
```

## Roles

| Role                                     | Description                                              |
| ---------------------------------------- | -------------------------------------------------------- |
| [common](roles/common)                   | Installs and configures packages like fail2ban, vim, etc |
| [ansible](roles/ansible)                 | Installs ansible                                         |
| [docker](roles/docker)                   | Starts Docker                                            |
| [teamspeak](roles/teamspeak)             | Starts a ts3server and sinusbot                          |
| [gotify](roles/gotify)                   | Starts [gotify/server](https://gotify.net)               |
| [traggo](roles/traggo)                   | Starts [traggo/server](https://github.com/traggo/server) |
| [ttrss](roles/ttrss)                     | Starts tiny tiny rss                                     |
| [nextcloud](roles/nextcloud)             | Starts [Nextcloud](https://nextcloud.com/)               |
| [nginx-tls-proxy](roles/nginx-tls-proxy) | Starts a nginx proxy and a companion for tls             |
| [sysupdate](roles/sysupdate)             | Does a sysupdate and reboots                             |
