# install-tuareg

Script d'installation de Tuareg+Company+Merlin pour les TPs OCaml,
écrit en bash et utilisant
[opam-boot](https://github.com/avsm/opam-boot)

## Utilisation

- Téléchargez le script
  [`install-tuareg-pfita.bash`](install-tuareg-pfita.bash)
- Sauvegardez-le dans le dossier de votre choix (par exemple `PFITA`)
- Ouvrez un terminal (dans le dossier `PFITA`) et exécutez les
  commandes :  
  ```
  chmod a+x install-tuareg-pfita.bash  
  ./install-tuareg-pfita.bash
  ```

## Remarques

- Ce script interactif conçu pour GNU/Linux suppose que les logiciels
  `ocaml` (4.00 <= version < 4.03) et `emacs` (version 24 ou 25) sont
  déjà installés.
- Il demande si vous souhaitez installer Merlin (mode Emacs améliorant
  Tuareg). Dans ce cas le script aura aussi besoin de `wget` et `m4`
  (ainsi que du paquet `build-essential`) pour installer Merlin.
- Pour installer ces paquets sous Ubuntu 16.04 ou Debian 9, faire :  
  ```
  sudo apt-get install build-essential m4 wget emacs24 ocaml-core ocaml-best-compilers
  ```
- Le script installe, si demandé, Merlin dans le dossier courant (dans
  un sous-dossier `_pfita`), puis la dernière version de Tuareg et
  Company, automatiquement à partir de [MELPA](https://melpa.org/).
- Ce sous-dossier `_pfita` ne pourra pas être déplacé vers un autre
  emplacement car les exécutables obtenus ont leur chemin absolu codé
  en dur. Si vous souhaitez néanmoins le déplacer, il faudrait alors
  supprimer ce dossier `_pfita`, déplacer le script
  `install-tuareg-pfita.bash` dans le dossier parent souhaité et le
  ré-exécuter.
- Le script ajoute enfin une configuration par défaut pour Emacs dans
  le fichier `~/.emacs.d/init.el` (qui est renommé s'il existe déjà)
- Si nécessaire, le script peut être relancé sans problème (par
  exemple pour passer de la configuration Tuareg+Company à
  Tuareg+Company+Merlin ou vice-versa)
