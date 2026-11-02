# MiniTV Live v9 — catalogue nettoyé + dépannage Euronews

## Changements

- Supprimées du catalogue intégré : ATV 1, ATV 2, ATV 3, Shalom TV.
- Une liste personnelle ancienne portant ces noms est également exclue à la lecture et à l'import M3U ; les favoris correspondants sont nettoyés automatiquement.
- Euronews Français : une adresse CDN Euronews répertoriée, deux sources de secours (Samsung/Wurl et Netplus), puis l'ancienne adresse. Toutes restent à vérifier sur l'appareil.
- CNEWS : conservée, mais marquée « accès à vérifier ». Le 403 provenait d'un refus du diffuseur pour l'intégration ; aucun accès non autorisé ni ancien embed Dailymotion cassé n'est ajouté. Pour une intégration complète, il faudrait une URL de lecture autorisée ou un Player ID fourni par le diffuseur.
- France 24, ARTE, BFM TV, BFM Business, 20 Minutes TV et TV5MONDE Info conservées.
- Même design, favoris, moteur hls.js et fenêtre flottante.

## Confiance des résultats

Tests syntaxiques et interface locale uniquement. Les URL ne sont pas certifiées lisibles ni disponibles depuis tous les pays. Le site statique GitHub Pages ne relaie pas les vidéos. La lecture réelle doit être validée sur l'appareil.

Sources :
- https://github.com/iptv-org/iptv
- https://database.freetuxtv.net/webStream/index
- https://faq.dailymotion.com/hc/en-us/articles/115008959787-Embed-your-content
