# docker-wp

## Initialisation de l'environnement de développement

 Créons un dossier où l'on mettera toutes les sources de nos sites en cours de développement. Imaginons sur notre disque dur avoir créer un dossier /site-dev. Il faut y placer, dans un dossier /docker le contenu du github cité ci-dessus.

 Lancer Docker toolbox, puis créons une nouvelle machine virtuelle :

    docker-machine create dev

 Connexion à la machine via ssh

    docker-machine ssh dev
    
 On créer le répertoire /var/www et on fait le point de montage
  
    mkdir /var/www
    sudo mount -t vboxsf nomdemonrepertoire /var/www

 Installation de docker-compose
  
    sudo -i
    curl -L https://github.com/docker/compose/releases/download/1.4.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
    chmod +x /usr/local/bin/docker-compose
    cp /usr/local/bin/docker-compose /var/lib/boot2docker/docker-compose

 On copie de script bootlocal.sh pour que les modifications restent persistantes au redemarrage
  
    sudo cp docker/bootlocal.sh /var/lib/boot2docker/bootlocal.sh
