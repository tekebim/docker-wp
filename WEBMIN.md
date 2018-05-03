# Installation de webmin
## Sous ubuntu

### Ajouyrt webmin repository dans les sources manager

Ouvrir avec l editeur :
    sudo nano /etc/apt/sources.list
    
Ajouter la ligne suivante en fin du fichier :
    deb http://download.webmin.com/download/repository sarge contrib
    
Enregistrer le fichier

Ajouter webmin PGP Key

    wget http://www.webmin.com/jcameron-key.asc
    sudo apt-key add jcameron-key.asc
 
Mettre a jour la liste des paquets pour inclure webmin repository

    sudo apt-get update

Installer webmin

    sudo apt-get install webmin
