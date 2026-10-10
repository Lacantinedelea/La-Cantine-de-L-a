# La Cantine de Léa — site web

## Ce que contient ce dossier

    la-cantine-de-lea/
      index.html      ← la page complète
      images/         ← les 10 photos (à déposer ici)

## 1. Les photos

Les photos des plats sont déjà dans le dossier `visuels/`, nommées d'après
chaque plat (`curry-japonais.jpg`, `pad-thai-aux-crevettes.jpg`…).
Elles s'affichent en vignette à côté du plat sur la carte, en grand quand
on touche la vignette, et dans la grande photo du haut et la mosaïque.

Pour ajouter la photo d'un nouveau plat : la déposer dans `visuels/` avec
un nom en minuscules, sans accents ni espaces, puis me demander de la
brancher sur la carte.

Il ne manque qu'une photo, à déposer dans `images/` :

| Fichier attendu | Ce que c'est |
|---|---|
| images/lea.jpg | le portrait de Léa, plutôt vertical |

Poids conseillé : moins de 500 Ko par photo.

## 2. Vérifier sur son ordinateur

Double-cliquer sur `index.html`. La page s'ouvre dans le navigateur.
Si des cadres restent vides, c'est qu'un nom de fichier ne correspond pas.

## 3. Mettre en ligne

Option A — Netlify (gratuit, 5 minutes)
1. Créer un compte sur netlify.com
2. Aller sur app.netlify.com/drop
3. Glisser le dossier `la-cantine-de-lea` entier (pas le zip, pas seulement
   index.html) dans la zone de dépôt
4. Le site est en ligne. Site configuration → Change site name pour choisir
   l'adresse, par exemple lacantinedelea.netlify.app

Pour une adresse en .fr, acheter le domaine (environ 10 €/an chez OVH ou
Gandi) puis le relier dans Netlify : Domain management → Add a domain.

Option B — chez un hébergeur classique
Envoyer le contenu du dossier à la racine du serveur par FTP.

## 4. Modifier le texte plus tard

Ouvrir `index.html` avec un éditeur de texte (Bloc-notes, TextEdit, ou
mieux : Visual Studio Code, gratuit). Chercher le texte à changer, le
remplacer, enregistrer, et redéposer le dossier sur Netlify.

## À finir avant la mise en ligne

- [ ] Compléter les mentions légales (lien en bas de page) : nom complet,
      adresse, statut, SIRET, date de déclaration DDPP, hébergeur
- [ ] Vérifier une par une les pastilles d'allergènes sous chaque plat
- [ ] Remplacer les trois encadrés en pointillés par de vrais avis clients
- [ ] Confirmer : délai du jeudi soir, absence de minimum de commande,
      moyens de paiement acceptés
- [ ] Déclarer l'activité auprès de la DDPP de Haute-Garonne si ce n'est
      pas déjà fait

## Bon à savoir

Le formulaire ouvre la messagerie du visiteur avec un message pré-rempli.
Rien n'est enregistré sur un serveur, rien n'est payé en ligne.
Le panier se vide si la page est rechargée : c'est normal pour un site
de ce type.
