# Préparation de la VM
## Sécurité
### Linux

* Chiffrement du disque dur : Avec l'option "Swap (no Hibernate)"
* Mise à jour de l'OS et des paquets : `sudo apt update -y && sudo apt full-upgrade -y && sudo apt autoremove -y && sudo apt autoclean -y`

### Windows (Prendre une version developper de l'OS)

* Chiffrement du disque dur
* Mise à jour de l'OS : `Install-WindowsUpdate -AcceptAll`
* Installation de Chocolatey : `Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))`
* Mise à jour de Chocolatey : `choco upgrade chocolatey -y `
* Installation de Windows Subsystem for Linux  (WSL) pour permettre l'exécution d'une distribution linux sous forme de conteneur : `choco install WSL2`
* Ajouter des exlusions dans Windows Defender pour ne pas être bloquer par l'antivirus : `Add-MpPreference -ExclusionPath "C:\Users\your user here\AppData\Local\Temp\chocolatey\"`

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
