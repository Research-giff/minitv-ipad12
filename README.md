# MiniTV Live v4 — Direct intégré

Application de télévision web autonome. Interface claire, navigation par cartes, favoris et recherche.

## Catalogue

- France 24 (français et anglais), ARTE, BFM TV, BFM Business et 20 Minutes TV : flux HLS directs.
- CNEWS : direct de son compte **officiel Dailymotion** intégré dans la page (`x3b68jn`) : pas de redirection vers un site de télévision.
- Suriname : ATV 1, ATV 2, ATV 3 et Shalom TV : adresses HLS publiques répertoriées.
- Trishul TV, Africanews, Africa 24, Apintie TV et tous les raccourcis sans lecteur intégré ont été retirés.

## Précisions

CNEWS utilise un lecteur vidéo embarqué, contrairement aux autres chaînes lues via le lecteur natif. Son fonctionnement dépend de Dailymotion et du navigateur utilisé.

Les adresses HLS surinamaises proviennent de listes publiques et d'infrastructures associées aux diffuseurs. Leur disponibilité **n'a pas pu être validée par lecture réelle** sur l'appareil de destination. Une liste publique n'est pas une preuve d'autorisation de redistribution commerciale. Pas de contournement de DRM, d'authentification ou de géoblocage.

Les données privées (favoris et playlists ajoutées) restent dans le stockage local de l'appareil. Seules les URLs vidéo directes HTTPS sont ajoutables.

## Publication

Décompresser l'archive, puis lancer `bash minitv-live-v4/publier.sh` depuis le dossier contenant le projet. Le script utilise le compte GitHub déjà authentifié, récupère un dépôt propre, copie les nouveaux fichiers, vérifie puis publie sur `main`. La lecture des chaînes doit être validée séparément.

Sources : https://www.dailymotion.com/video/x3b68jn ; https://github.com/iptv-org/iptv/blob/master/streams/sr.m3u ; https://www.telesur.sr/atv/ ; https://gist.github.com/giomaniego-dev/5d5e671a09514c5011ba4b54289b0b95
