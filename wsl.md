# Windows Subsystem for Linux (WSL)<!-- omit in toc -->

## Sommaire<!-- omit in toc -->

- [Différences entre Linux et Windows](#différences-entre-linux-et-windows)
- [Intérêts](#intérêts)
- [Installation](#installation)

## Différences entre Linux et Windows

## Intérêts

|     | Dual boot | Machine virtuelle | WSL |
| --- | --------- | ----------------- | --- |
|     |           |                   |     |

## Installation

- ouvrir le Powershell en tant qu'administrateur
- activer les fonctionnalités WSL avec la commande :

```bash
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

- activer les fonctionnalités de machine virtuelle avec la commande :

```bash
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

- rédémarrer l'ordinateur
- télécharger le package WSL2 <https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi>
- installer ce package
- ouvrir une nouvelle fenêtre Powershell et installer la commande WSL :

```bash
wsl --install
```

- configurer WSL pour être sur la version 2 :

```bash
wsl --set-default-version 2
```

- lister les distributions Linux disponibles avec :

```bash
wsl --list --online
```

- installer la distribution voulue avec :

```bash
wsl --install -d <Distribution Name>
```
