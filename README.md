# Exercice03-TestMSc
Déploiement d’une stack WordPress utilisant Docker, Nginx, PHP-FPM et MariaDB.
L’objectif est de mettre en place une architecture fonctionnelle avec un volume partagé contenant les données et les configurations nécessaires.

## Services
- Nginx 1.27-alpine : serveur web servant les fichiers WordPress.
- PHP-FPM 8.3 (image personnalisée) : exécution du code PHP avec les extensions nécessaires.
- MariaDB 11.4 : base de données utilisée par WordPress.
- wp-setup (conteneur temporaire) : téléchargement automatique de la dernière version de WordPress dans le volume partagé.

## Étapes
1. Préparation de l’environnement
2. Téléchargement de WordPress
3. Construction de l’image PHP
4. Démarrage de la stack
5. Installation WordPress
6. Vérifications
