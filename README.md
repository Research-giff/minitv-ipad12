# MiniTV Live v8 — diagnostic de lecture et moteur HLS

Cette version corrige le lecteur, sans changer l’interface ni supprimer des chaînes ou favoris.

- Ajout de hls.js 1.5.20, chargé uniquement lorsque le navigateur ne prend pas en charge HLS nativement. Deux CDN publics servent de redondance, et aucune requête n’est nécessaire sur Safari natif.
- BFM TV / BFM Business : sources d’origine et secours conservés, désormais exploitables sur Chrome/Firefox si les serveurs et règles CORS le permettent.
- CNEWS : le HLS CANAL+ reste comme source candidate. Les embeds Dailymotion legacy sans Player ID ont été retirés car ils renvoient HTTP 403 (exigence Dailymotion septembre 2026). La chaîne demeure visible, mais la disponibilité directe n’est pas garantie.
- Sur les iframes, « page chargée » ne signifie plus « lecture confirmée ». Le mini-lecteur ne flotte qu’après l’événement de lecture vidéo confirmée.
- L’application affiche des raisons concrètes lorsqu’un flux HLS échoue (réseau, CORS, manifeste, codec).
- Tous les 13 canaux et les favoris (`minitv-live-v5-clean`) sont préservés. Rien n’est retransmis par le Raspberry Pi.

## Limites

Il n’est pas possible de transformer un 403 du diffuseur en autorisation d’accès. Aucune lecture réelle sur le matériel de l’utilisateur n’a été démontrée. L’utilisation d’un CDN hls.js nécessite un accès Internet et peut être bloquée par un filtrage réseau.

Sources : https://developers.dailymotion.com/changelog/api-player-id-required-in-embed-urls ; https://github.com/video-dev/hls.js
