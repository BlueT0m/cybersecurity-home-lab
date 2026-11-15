
# Cybersecurity Home Lab

## Présentation

Projet personnel de cybersécurité réalisé dans un laboratoire virtuel isolé.

Objectif : apprendre les méthodes de reconnaissance réseau, d'énumération et d'audit de sécurité.

## Environnement

- Kali Linux
- Metasploitable 2
- Oracle VirtualBox
- Réseau Host-only
- Nmap
- enum4linux
- smbclient

## Travaux réalisés

- Installation et configuration du laboratoire.
- Configuration du réseau isolé.
- Reconnaissance réseau avec Nmap.
- Identification des services et de leurs versions.
- Vérification de l'accès FTP anonyme.
- Énumération des partages SMB.
- Analyse des permissions.
- Rédaction d'un rapport de sécurité.

## Principaux constats

- Accès FTP anonyme autorisé.
- Connexion SMB anonyme autorisée.
- Partage SMB tmp accessible en lecture.
- Signature SMB désactivée.
- Présence d'un service bindshell sur le port 1524.

## Rapports

Consulter le dossier `reports/` pour les résultats détaillés.

## Cadre des tests

Tous les tests ont été réalisés sur une machine Metasploitable 2 personnelle, dans un réseau virtuel isolé.

Aucune cible externe n'a été testée.

## Auteur

Projet personnel d'apprentissage du pentest éthique.
