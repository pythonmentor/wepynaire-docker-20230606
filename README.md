# Comment conteneuriser votre application Django à l'aide de Docker

Dans ce WePynaire, une application Django simple a été conteneurisée. Cela signifie que 
nous allons écrire ensemble un fichier Dockerfile simple pour créer une image Docker avec 
le code de notre mini-application exemple.

Les étapes d'écriture du Dockerfile sont expliquées en détails [dans la vidéo de l'atelier](https://vimeo.com/833566075?share=copy).

## Construction de l'image à partir du fichier Dockerfile

Une fois que le fichier Dockerfile est redigé, on construit l'image docker avec la commande `docker compose build`.

## Démarrage des containers

Le démarrage des conteneurs django et postgresql est piloté par docker compose. Il vous suffit d'utiliser la commande `docker compose up` pour le démarrage, et `docker compose down` pour l'arrêt.
