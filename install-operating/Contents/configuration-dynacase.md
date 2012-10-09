# Configureation Dynacase

## Configuration de Dynacase pour utiliser TE

Pour que Dynacase puisse utiliser TE pour la transformation de documents, et l'indexation plein-texte de ceux-ci, il faut positionner les paramètres applicatifs suivants :

| Application | Paramètre | Valeur | Détail |
| ----------- | --------- | ------ | ------ |
| "bibliothèque dynacase" | "Adresse du serveur de transformation" | `127.0.0.1` | L'adresse d'écoute du serveur TE. |
| "bibliothèque dynacase" | "Numéro de port du serveur de transformation" | `51968` | Le port d'écoute du serveur TE. |
| "bibliothèque dynacase" | "Activation du serveur de transformation" | `yes` | Activation/désactivation de l'utilisation du serveur TE par les transformation de documents Dynacase. |
| "bibliothèque dynacase" | "URL pour les callback du serveur de transformation" | Exemple : `http://nom_du_serveur/nom_du_contexte/index.php` | L'URL d'accès à votre serveur Dynacase par laquelle TE interagira en retour. Il est important de spécifier l'argument `authtype=basic` afin que TE puisse s'authentifier correctement sur Dynacase avec le compte définit dans `te.conf` (URL_CALLBACK_LOGIN/URL_CALLBACK_PASSWORD) |
| "bibliothèque dynacase" | "Activation de l'indexation plein texte avec TE" | `yes` | Activation/désactivation de l'utilisation du serveur TE pour indexer les fichiers (n'est pris en compte que si "Activation du serveur de transformation" est positionné à "yes"). |