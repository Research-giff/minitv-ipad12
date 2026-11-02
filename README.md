# MiniTV Live v6 — dépannage des directs

Version v5 conservée visuellement, avec 11 chaînes intégrées et favoris préservés dans `minitv-live-v5-clean`.

## Changement de lecture

- CNEWS : lecteur Dailymotion direct, endpoint `geo.dailymotion.com/player.html?video=x3b68jn` et possibilité de basculer manuellement vers le lecteur hérité. Le contenu est fourni par le compte officiel CNEWS ; nous ne contrôlons ni son lecteur ni sa compatibilité.
- BFM TV et BFM Business : leur flux existant reste la source principale ; un flux SFR public documenté est ajouté comme source de secours. L'accessibilité varie.
- ATV 1, ATV 2 et ATV 3 : HLS historique conservé, secours via les lecteurs ATV relayés par Suricloud/Telesur. La compatibilité en iframe n'est pas garantie.
- ARTE : HLS d'origine conservé. Certains programmes ou flux sont soumis au géoblocage, aucune méthode de contournement intégrée.
- Autres chaînes et favoris : inchangés.

## Diagnostic et limites

- Le message sous le lecteur indique **la source essayée** et l'erreur vidéo (code 1/2/3/4, etc.).
- Au bout de 18 secondes sans données, un flux HLS non chargé bascule sur le secours s'il existe.
- Le bouton **« Source suivante »** permet de changer manuellement de source ; utile pour CNEWS et les lecteurs IPTV.
- Le chargement d'un lecteur intégré (iframe) ne prouve **pas** qu'une vidéo est en cours.
- Aucune lecture n'a été vérifiée physiquement sur le matériel de l'utilisateur : tests de code et d'interface uniquement.
- Les flux HTTP, protégés par DRM, ou avec compte ne sont pas contournés.
- L'application est une interface statique sur GitHub Pages : aucune vidéo ne passe par le Raspberry Pi.
