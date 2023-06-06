# Comment conteneuriser votre application Django à l'aide de Docker

Dans ce WePynaire, une application Django simple a été conteneurisée. Cela signifie que 
nous allons écrire ensemble un fichier Dockerfile simple pour créer une image Docker avec 
le code de notre mini-application exemple.

<div style="padding:75% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/833566075?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Comment conteneuriser votre application Django à l'aide de Docker et dans quel but (Partie 2)"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

Les étapes d'écriture du Dockerfile sont expliquées en détails dans la vidéo de l'atelier.

## Construction de l'image à partir du fichier Dockerfile

Une fois que le fichier Dockerfile est redigé, on construit l'image docker avec la commande `docker compose build`.

## Démarrage des containers

Le démarrage des conteneurs django et postgresql est piloté par docker compose. Il vous suffit d'utiliser la commande `docker compose up` pour le démarrage, et `docker compose down` pour l'arrêt.