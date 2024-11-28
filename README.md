# App-e-commerce : Prestashop

1- Installations
- Java
  sudo apt update
  sudo apt install fontconfig openjdk-17-jre

- Jenkins
  curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
    /usr/share/keyrings/jenkins-keyring.asc > /dev/null
 
  echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
    https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
    /etc/apt/sources.list.d/jenkins.list > /dev/null
 
   sudo apt-get update
   sudo apt-get install jenkins
  
  * activer le service Jenkins
 
    sudo systemctl enable jenkins
    sudo systemctl start jenkins
    sudo systemctl status jenkins
 
  * Récuperer le mot de passe
    sudo cat /var/lib/jenkins/secrets/initialAdminPassword

  * Pour voir le Jenkins : localhost:8080

- Prestashop via docker compose
 
Docker
 
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
apt-cache policy docker-ce
sudo apt install docker-ce
sudo systemctl status docker
sudo usermod -aG docker ${USER}
su - ${USER}
groups
sudo usermod -aG docker username
 
Docker-compose
sudo curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/bin/docker-compose && sudo chmod +x /

2- Création des fichiers 

- docker-compose.yml : pour créer le projet Prestashop
- Jenkinsfile : pour définir les étapes de pipeline de manière déclarative

3- Création du projet dans GitLab

- git init
- git add .
- git commit -m 'first commit'
- git branch
- git remote add origin https://github.com/hermann85/prestashop.git
- git push -u origin master

4- Jenkins (configurations)

- Lien du dépôt GitLab : xxxxxxxxxxxxxxxxxx

5- Lancement de l’installation par Jenkins 
  * Etapes de l’installation du site prestashop
  * Le résultat du test fonctionnel du Titre et du Menu 

6- Lancement de la page boutique partie la plus importante 
  * Etapes d’installation de la boutique 
  * Le résultat du test fonctionnel du menu de la boutique






