# Applications dans le terminal (TUI, CLI, ...)

## Définitions

- TUI : Terminal User Interface
 - un logiciel qui se lance depuis le terminal
 - qui possède une interface limitée
 - navigation avec combinaison de touches, parfois avec la souris
- GUI : Graphical User Interface
 - un logiciel qui se lance depuis le bureau
 - qui possède une interface complète
 - navigation à la souris

## Pourquoi privilégier l'un ou l'autre ?

### GUI

- pour utilisateurs débutant ou intermédiaire
- pour se former
- pour utiliser sur son ordinateur
- pour être productif immédiatement
- pas de contraintes de ressources (RAM, CPU)

### TUI

- pour utilisateurs intermédiaires ou avancés
- pour épurer et simplifier l'UX
 - se concentrer sur sa tâche en cours et ne pas se laisser distraire
 - ne plus se perdre dans plusieurs fenêtres
- pour utiliser sur un serveur distant en SSH
- pour limiter les besoins en ressources (RAM notamment)
- pour gagner en productivité une fois les raccourcis appris et sa mémoire musculaire entrainée

### Editeurs pour terminal

#### Editeurs légers

- nano
 - installé par défaut sur la plupart des systèmes UNIX
 - interface simple et austère
 - navigation au clavier principalement avec combinaisons de touches propriétaires
- micro
 - à installer soi-même
 - interface avec coloration syntaxique
 - navigation à la souris et au clavier avec des combinaisons de touches intuitives

#### "IDE"

- logiciels se rapprochant d'un IDE avec
 - coloration syntaxique
 - gestion de fichiers
 - linter
 - formater
 - LSP
- exemples :
 - nvim
 - helix
 - kakoune
 - emacs

### Explorateur de fichiers

- nnn
- fzf

### git

- gh
 - pour communiquer directement avec github depuis son terminal
  - création de repo, de PR, d'issue, ...
 - uniquement des commandes à lancer, pas d'interface
- gitui ou lazygit
 - comme supplément de gitkraken ou github desktop
 - interface avec navigation à la souris et avec des combinaisons de touches

### Docker via le terminal

- lazydocker
 - comme supplément à docker desktop
  - ne remplace pas le daemon de docker-ce, fourni avec docker desktop et parfois nécessaire selon votre système
 - interface avec navigation à la souris et avec des combinaisons de touches

### "Navigateur"

- s
 - pour lancer une recherche avec différents moteurs sur votre navigateur
- lynx ou w3m
 - comme supplément à un navigateur

### Requêtes API dans un terminal

- atac
 - comme supplément à postman ou insomnia
 - interface avec navigation à la souris et avec des combinaisons de touches

### Base de données

- usql
 - permet de se connecter à une BDD via un DSN
