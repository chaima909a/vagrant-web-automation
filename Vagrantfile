# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  # Nom et box utilisée
  config.vm.box = "ubuntu/jammy64"

  # Nom du projet
  config.vm.hostname = "webserver-vagrant"

  # Adresse IP statique
  config.vm.network "private_network", ip: "192.168.77.11"

  # Synchronisation du dossier courant avec la VM (optionnel)
  config.vm.synced_folder ".", "/var/www/html"

  # Script de provisionnement (installation automatique)
  config.vm.provision "shell", inline: <<-SHELL
    echo "🔧 Mise à jour du système..."
    apt-get update -y

    echo "🌐 Installation d'Apache et Git..."
    apt-get install -y apache2 git

    echo "📁 Clonage du site web depuis GitHub..."
    cd /var/www/html
    git clone https://github.com/USERNAME/mon-site-web.git .
    
    echo "🧰 Configuration des permissions..."
    chown -R www-data:www-data /var/www/html
    chmod -R 755 /var/www/html

    echo "🚀 Redémarrage du service Apache..."
    systemctl restart apache2

    echo "✅ Déploiement terminé ! Site disponible sur http://192.168.77.11"
  SHELL
end
