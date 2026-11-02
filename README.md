# MiniTV Live v7 — sources IPTV et reprise des directs

Interface de v6 et fenêtres flottantes conservées. Le catalogue passe de 11 à 13 entrées.

## Changements

- **BFM TV** : conserve le flux CDN existant, le secours SFR présent en v6, ajoute une troisième URL CDN CloudFront citée par une playlist tierce.
- **BFM Business** : conserve les deux sources (CDN et SFR). L'URL SFR est déjà dans v6 et n'est pas importée une seconde fois.
- **CNEWS** : essai HLS depuis le domaine CDN CANAL+, puis deux lecteurs Dailymotion intégrés. Le flux CANAL+ peut nécessiter un jeton, être géobloqué ou échouer ; il n'est pas certifié fonctionnel.
- **20 Minutes TV** : secours Digiteka tiré de `garelp/iptv-playlists/fr.m3u`.
- **Euronews Français et TV5MONDE Info** : deux flux directs HTTPS supplémentaires répertoriés publiquement ; disponibilité non garantie, TV5MONDE peut être géobloqué.
- **ATV, ARTE, Shalom, France 24 et favoris** : préservés, même identifiants et même stockage local.

## Sources consultées

- https://github.com/garelp/iptv-playlists/blob/main/fr.m3u
- https://github.com/Fraewin/iptv/blob/main/playlist.m3u
- https://github.com/Free-TV/IPTV/blob/master/lists/france.md

La playlist CNEWS du dépôt `garelp` pointe vers un fichier GitHub 404 et n'est **pas** réutilisée. Aucun accès IPTV privé ou chaîne payante ne fait partie de ce correctif. Une URL publiée sur GitHub n'est ni une garantie de lecture ni une licence de redistribution.

Les sources ont été vérifiées **statiquement** dans des catalogues publics ; leur lecture HTTP réelle et leur décodage sur l'appareil ne sont pas confirmés. Dans MiniTV, utiliser « Source suivante » si un flux échoue.
