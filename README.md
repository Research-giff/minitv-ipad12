# MiniTV Live — iPad Edition

Une mini-application web personnelle de télévision en direct, conçue pour **Safari sous iOS 12.5.7** (iPad mini 2, Apple A7, 1 Go RAM).

**Pas de Raspberry Pi nécessaire pendant la lecture.** L'iPad télécharge les segments HLS directement depuis les serveurs externes des chaînes.

## Fonctions

- Lecteur vidéo **natif Safari / HLS `.m3u8`**, sans hls.js et sans transcodage ;
- 8 flux de démonstration publiquement répertoriés (France 24 FR/EN, ARTE, BFM TV, Africanews FR, Africa 24, BFM Business, 20 Minutes TV) + lien vers CNEWS officiel ;
- Favoris, catégories, recherche, ajout d'une chaîne HTTPS ;
- Importation de listes **M3U locales** via un fichier sélectionné sur l'iPad (limite 200 chaînes personnalisées) ;
- Sauvegarde locale sur l'iPad avec `localStorage` ;
- Aucune dépendance CDN JavaScript, aucune publicité, aucun serveur/proxy, aucun compte ;
- Écran d'accueil iOS (« Sur l'écran d'accueil » dans Safari), mode plein écran vidéo.

## Déploiement sur GitHub Pages

1. Sur github.com, crée un dépôt public, par exemple `minitv-ipad12`.
2. Ajoute **à la racine du dépôt** `index.html`, `icon-180.png` et ce `README.md` (tu peux aussi ajouter `exemple.m3u`).
3. Dans `Settings → Pages`, choisis `Deploy from a branch`, branche `main`, dossier `/(root)`, puis `Save`.
4. Ouvre sur l'iPad `https://TON_COMPTE.github.io/minitv-ipad12/`.
5. Dans Safari iOS 12, touche « Partager » → « Sur l'écran d'accueil ».
6. Choisis une chaîne. Si Safari bloque le lancement automatique, touche ▶.

Cette procédure met en ligne **uniquement l'interface HTML statique**. Il n'existe aucun backend : ni le Pi, ni le compte GitHub ne retransmettent les vidéos.

Pour une utilisation totalement locale hors hébergement, un serveur HTTP local ou une app native serait nécessaire pour l'accès à l'interface; les **flux vidéo**, eux, exigent toujours Internet.

## Ajouter CNEWS

Le projet contient un raccourci vers le site officiel `https://www.cnews.fr/`, sans présumer d'une URL HLS directe, stable et autorisée. Si tu possèdes une URL HTTPS de direct accessible légalement, ajoute-la avec `+ Chaîne → Flux HLS`.

## Compatibilité et limites

- La prise en charge **HLS native** est assurée par Safari iOS, mais les flux tiers changent souvent de disponibilité et peuvent être **géobloqués**, expirer ou exiger des cookies, jetons, en-têtes ou DRM.
- L'intégration **ne contourne pas** les protections, connexions ou restrictions géographiques. Elle n'héberge ni ne relaie de contenu.
- Pour les flux HTTP anciens, GitHub Pages utilise HTTPS et les bloquera souvent (mixed content) : seuls les flux HTTPS sont acceptés par l'app.
- L'importation locale d'un `.m3u` marche mieux que la récupération distante (CORS).
- iOS 12 a un moteur WebKit ancien : certains codecs modernes (AV1, HEVC selon matériel, etc.) peuvent échouer.
- Un direct fonctionne via `video.src` si Safari sait décoder le flux. Aucune garantie de lecture de chaque adresse ; utilise le bouton « Ouvrir le direct » comme repli.
- Pour les contenus protégés, utilise le service ou l'application officiel(le).
- La playlist de démonstration suit les adresses répertoriées dans le projet [IPTV-org](https://github.com/iptv-org/iptv/blob/master/streams/fr.m3u), consultées le 2 novembre 2026. Ce répertoire ne constitue pas une licence de redistribution. Vérifie les conditions de chaque chaîne avant toute publication commerciale.

## Développement

HTML/CSS/JavaScript autonome, sans compilation. Pour tester sur un ordinateur : `python3 -m http.server 8000` puis `http://localhost:8000` ; cette étape n'est pas nécessaire une fois le site sur GitHub Pages.

**Statut : MVP de code prêt à déployer, non testé physiquement sur l'iPad de l'utilisateur.**

Projet indépendant non affilié à Molotov TV ni aux chaînes.
