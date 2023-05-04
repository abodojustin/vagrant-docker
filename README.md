# Vagrant-docker

Ce dossier contient deux fichiers à savoir:
> - un Vagrantfile qui va provisionner une machine CentOS
> - et enfin un script qui va nous permettre d'installer docker

Si ce script ne fonctionne pas pour une raison ou une autre, vous pouvez l'installer manuellement à l'aide des commandes suivantes:

``
curl -fsSL https://get.docker.com -o get-docker.sh
``

``
sudo sh get-docker.sh
``

Ensuite vous allez devoir ajouter votre utilisateur au groupe __docker__ à l'aide de la commande suivante:
``sudo usermod -aG docker vagrant``

Ensuite vous pouvez demarrer le service à l'aide de la commande:
``sudo systemctl start docker``

Enfin vous pouvez également démarrer le service au demarrage de la machine:
``sudo systemctl enable docker``

Pour vérifier que tout fonctionne très bien vous pouvez exécuter la commande:
``docker --version``

``docker run hello-world``: pour lancer notre premier conteneur :grin:
