# MiniTV Live v5 — mini-lecteur flottant et catalogue propre

## Changements

- Mini-lecteur flottant en bas à droite dès que l'utilisateur descend et que le direct est lancé (HLS), ou que le lecteur CNEWS a chargé son contenu.
- Aucun lecteur dupliqué : le même élément vidéo ou la même iframe reste actif pendant le défilement.
- Icônes : agrandir (↗) retourne au lecteur principal ; fermer (×) arrête la lecture et ferme le mini-lecteur.
- Version de stockage local neuve (`minitv-live-v5-clean`), sans réimporter les anciennes chaînes et favoris obsolètes.
- Bouton `Nettoyer ma liste` pour supprimer les imports et favoris de la version courante.
- Catalogue initial : France 24 FR/EN, ARTE, BFM TV, BFM Business, 20 Minutes TV, CNEWS (iframe Dailymotion), ATV 1/2/3 et Shalom TV du Suriname.
- Pas de Trishul, Africanews, Africa 24, ni de liens vers des sites servant de substituts au direct.
- Aucune mention de modèle d’appareil ou de navigateur dans l’interface grand public.

Les liens vidéo sont fournis à titre de lecture ; une vérification syntaxique ne démontre ni leur accessibilité permanente ni leur décodage sur un appareil précis. Le lecteur CNEWS hébergé par Dailymotion peut refuser certains navigateurs. La fenêtre flottante fonctionne dans la page web ; elle ne reste pas au-dessus des autres applications.

## Installation

Décompresser le ZIP et lancer `bash minitv-live-v5/publier.sh` depuis le dossier de Téléchargements. Le script vérifie le contenu distant après publication. Ouvrir `https://research-giff.github.io/minitv-ipad12/?v=5`.

Les favoris et listes personnalisées précédentes ne sont pas restaurés volontairement dans la v5, afin de garantir le nettoyage. Les données anciennes ne sont pas effacées physiquement du navigateur.
