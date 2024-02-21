# Préparation de la VM
## Sécurité

* Chiffrement du disque dur : Avec l'option "Swap (no Hibernate)"
* Mise à jour de l'OS et des paquets : `sudo apt update -y && sudo apt full-upgrade -y && sudo apt autoremove -y && sudo apt autoclean -y`

## Logs

### Linux : 

* Date + la commande `PS1="\[\033[1;32m\]\342\224\200\$([[ \$(/opt/vpnbash.sh) == *\"10.\"* ]] && echo \"[\[\033[1;34m\]\$(/opt/vpnserver.sh)\[\033[1;32m\]]\342\224\200[\[\033[1;37m\]\$(/opt/vpnbash.sh)\[\033[1;32m\]]\342\224\200\")[\[\033[1;37m\]\u\[\033[01;32m\]@\[\033[01;34m\]\h\[\033[1;32m\]]\342\224\200[\[\033[1;37m\]\w\[\033[1;32m\]]\n\[\033[1;32m\]\342\224\224\342\224\200\342\224\200\342\225\274 [\[\e[01;33m\]$(date +%D-%r)\[\e[01;32m\]]\\$ \[\e[0m\]"`
* Script + la commande `"script fichier.log"`

### Windows : 

* `Start-transcript fichier.log`
  
## Documentation

* CherryTree : Pour la prise de note
* Flameshot : Pour les screenshots
* Peek : Pour créer des GIFs
