# 🖥️ Installation et Automatisation d’un Environnement Web avec Vagrant

## 🎯 Objectif
Mettre en place un serveur web fonctionnel sur une machine virtuelle **Ubuntu 22.04** en automatisant :
- L’installation d’**Apache** et **Git**  
- Le **clonage automatique d’un site web** depuis un dépôt GitHub  
- Le **déploiement** et la **configuration** via un fichier `Vagrantfile`

## 🧰 Outils utilisés
- **Vagrant**  
- **VirtualBox**  
- **Ubuntu 22.04 LTS (jammy64)**  
- **GitHub** pour héberger le projet web

## ⚙️ Étapes principales
1. Initialisation du projet avec `vagrant init`
2. Configuration du `Vagrantfile` :
   - Box : Ubuntu 22.04  
   - IP : 192.168.77.11  
   - Provisionnement automatique (Apache + Git + clone du dépôt)
3. Démarrage de la machine : `vagrant up`
4. Correction du problème “Index of /” → ajout du fichier `index.html`

## 🚧 Problèmes rencontrés et solutions
| Problème | Cause | Solution |
|-----------|--------|----------|
| `vagrant` non reconnu | Non présent dans le PATH | Utiliser `cmd.exe` et redémarrer |
| IP inchangée | VM existante non détruite | `vagrant destroy` puis `vagrant up` |
| “Index of /” affiché | Fichier `index.html` manquant | Renommer le fichier HTML principal |

## ✅ Résultats
- VM Ubuntu 22.04 fonctionnelle  
- Apache et Git installés  
- Site web accessible à : `http://192.168.77.11`

## 🧩 Compétences développées
- **Infrastructure as Code (IaC)** avec Vagrant  
- **Automatisation** de serveurs web  
- **Virtualisation** (VirtualBox)  
- **Résolution d’erreurs techniques**  
- **Premiers pas vers Ansible, Docker et Terraform**

---

✳️ *Projet réalisé par **Chayma ABIDI**, 2025.*
