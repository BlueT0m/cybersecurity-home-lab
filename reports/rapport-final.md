
# Rapport final d'audit de sécurité

## 1. Informations générales

- Projet : Cybersecurity Home Lab
- Cible : Metasploitable 2
- Adresse IP : 192.168.56.101
- Système d'analyse : Kali Linux
- Outils : Nmap, enum4linux, smbclient
- Environnement : VirtualBox, réseau Host-only isolé

## 2. Résultats de reconnaissance

Nmap a identifié plusieurs services accessibles :

- FTP : 21
- SSH : 22
- Telnet : 23
- HTTP : 80
- SMB : 139 et 445
- MySQL : 3306
- UnrealIRCd : 6667

## 3. Vulnérabilités et mauvaises configurations

### FTP

- Connexion anonyme autorisée.
- Aucun fichier supplémentaire trouvé à la racine FTP.
- Risque : accès non autorisé au service FTP.

### SMB

- Connexion anonyme autorisée.
- Partage tmp accessible en lecture.
- Signature SMB désactivée.
- Risque : exposition de fichiers et informations.

### Shell sur le port 1524

- Service identifié comme bindshell.
- Nmap indique un shell root exposé.
- Risque : critique si l'accès permet une session privilégiée.
- Aucune connexion au shell effectuée.

### Services anciens

Plusieurs services utilisent des versions anciennes.
Une vérification complémentaire est nécessaire pour confirmer leur exploitabilité.

## 4. Recommandations

- Désactiver les connexions FTP anonymes.
- Restreindre les accès aux partages SMB.
- Activer la signature SMB.
- Supprimer les services inutiles.
- Mettre à jour les logiciels.
- Restreindre les services privilégiés.

## 5. Conclusion

L'audit a révélé plusieurs mauvaises configurations sur Metasploitable 2.

Les tests ont été réalisés dans un laboratoire virtuel isolé et contrôlé.

Aucune cible externe n'a été testée.
