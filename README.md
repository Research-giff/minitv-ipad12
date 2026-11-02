# MiniTV Live — Version grand public v3

Application web statique adaptée à Safari iOS 12.5.7, sans serveur Raspberry Pi pendant la lecture.

## Nouveautés

- Nouvelle interface grand public : lecteur 16:9, cartes de chaînes, catégories, favoris et recherche.
- Retrait des chaînes **Africanews** et **Africa 24**.
- 6 entrées pour le **Suriname** : Trishul TV et Shalom TV en HLS, ATV 1/2/3 et Apintie TV via les lecteurs des diffuseurs.
- **CNEWS** : ouverture de sa page dédiée au direct sur Molotov, avec une alternative vers le catalogue officiel CANAL+. Il n'existe pas dans cette version de flux CNEWS HLS officiel validé et intégrable ; son visionnage dépend de leur service, des droits, du pays et de la compatibilité navigateur.
- Flux français conservés : France 24 FR/EN, ARTE, BFM TV, BFM Business et 20 Minutes TV.
- Favoris, import M3U (jusqu'à 200 entrées), ajout manuel de flux HTTPS et liens officiels.

## Installer

Dézippe cette archive sur le Raspberry Pi, puis lance `bash publier.sh` depuis le dossier extrait. Le script clone un dépôt propre, remplace `index.html` et `README.md`, puis publie sur la branche `main` via GitHub CLI. Il ne transfère pas de fichiers secrets et conserve les autres fichiers déjà publiés (notamment l'icône).

## Limites

Le déploiement GitHub Pages prouve la disponibilité de l'interface, **pas** la lecture de chaque chaîne. Les flux de tierces parties peuvent expirer, être géobloqués, demander un compte, utiliser des codecs incompatibles iOS 12 ou être protégés par des droits. Pas de contournement de DRM, d'abonnement ou de restriction. L'application n'héberge ni ne retransmet les images.

Sources : https://www.telesur.sr/atv/ · https://www.apintie.sr/livestream · https://www.canalplus.com/tab/live/all-channels · https://www.molotov.tv/fr_fr/c/2/cnews · https://github.com/iptv-org/iptv/blob/master/streams/sr.m3u
