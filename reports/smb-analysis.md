# Analyse SMB

Cible : Metasploitable 2
Adresse : 192.168.56.101
Outils : enum4linux, smbclient

## Résultats

- Connexion anonyme autorisée.
- Partage tmp accessible sans authentification.
- Lecture du contenu de tmp autorisée.
- Partages print$, opt et ADMIN$ refusés.
- Samba 3.0.20-Debian détecté.

## Risque identifié

Un utilisateur sans compte peut consulter le contenu du partage tmp.

## Recommandation

Limiter les accès anonymes et appliquer des permissions adaptées aux partages.
