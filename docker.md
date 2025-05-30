# Docker<!-- omit in toc -->

## Sommaire<!-- omit in toc -->

- [Historique de la virtualisation](#historique-de-la-virtualisation)
- [Intérêts](#intérêts)
- [Installation](#installation)
  - [Sur MacOS](#sur-macos)
  - [Sur Ubuntu](#sur-ubuntu)
  - [Sur Windows et WSL](#sur-windows-et-wsl)
  - [Utilisation sans sudo](#utilisation-sans-sudo)
- [Commandes principales](#commandes-principales)

## Historique de la virtualisation

1. Pas assez de puissance
   - 1 machine (serveur) === 1 application
2. Gain de puissance des machines
   - introduction des VM, pouvant faire tourner plusieurs systèmes sur une seule machine
   - 1 machine === x VM, une application par VM
   - réduction des coûts
     - besoin de moins de machines
3. Introduction de la containerisation
   - supprimer le surplus logiciel inutile des VM
   - se rapprocher du système hôte
   - 1 machine === x containers, une application par container
   - réduction des coûts
     - besoin de machines moins puissantes

## Intérêts

- réduction de l'utilisation de ressources

![différence entre VM et docker](https://www.opc-router.com/wp-content/uploads/2021/10/Docker_Vergleich-EN.png)

- partageable plus facilement entre développeurs
- gestion facilitée et simplifiée
- déployable directement sur des serveurs de production
- tester rapidement si son application est compatible sur différents environnements
- pouvoir développer son application dans un environnement clos, qui ne contamine pas le reste du système

## Installation

### Sur MacOS

Installer [docker desktop](https://docs.docker.com/desktop/setup/install/mac-install/)

### Sur Ubuntu

```bash
for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do sudo apt-get remove $pkg; done
```

```bash
sudo apt-get update
```

```bash
sudo apt-get install ca-certificates curl
```

```bash
sudo install -m 0755 -d /etc/apt/keyrings
```

```bash
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
```

```bash
sudo chmod a+r /etc/apt/keyrings/docker.asc
```

```bash
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

```bash
sudo apt-get update
```

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

### Sur Windows et WSL

Suivre les indications pour Ubuntu, puis installer [docker desktop](https://docs.docker.com/desktop/setup/install/windows-install/).

### Utilisation sans sudo

Utiliser docker avec `sudo` est une faille de sécurité. Une attaque peut démarrer dans un container et remonter dans l'ordinateur hôte.

Plus d'informations [ici](https://docs.docker.com/engine/security/#docker-daemon-attack-surface).

C'est pourquoi il faut utiliser docker sans sudo :

```bash
sudo groupadd docker
```

```bash
sudo usermod -aG docker $USER
```

```bash
newgrp docker
```

## Commandes principales

https://cht.sh/docker

https://cht.sh/docker-compose