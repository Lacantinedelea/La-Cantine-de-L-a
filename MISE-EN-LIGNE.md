# Mettre le site en ligne, étape par étape

Compte environ 30 minutes. Tu n'as rien à installer.

---

## Pour comprendre en une phrase

Le site est un dossier de fichiers. Netlify est la maison où on range ce
dossier. Le nom de domaine `.fr` est la plaque qu'on visse sur la porte
pour que les gens trouvent la maison.

On fait donc trois choses, dans cet ordre : préparer le dossier,
le déposer dans la maison, visser la plaque.

---

## Avant de commencer

Prépare trois choses :

1. Le dossier `la-cantine-de-lea` sur ton ordinateur, avec les photos
   déjà déposées dans `images/` (voir LISEZ-MOI.md)
2. Une adresse mail et un mot de passe pour créer un compte
3. Tes identifiants du site où tu as acheté le domaine
   (OVH, Gandi, IONOS… c'est là que tu as payé)

---

## Étape 1 — Vérifier que le site marche

Double-clique sur `index.html`.

Le site s'ouvre dans ton navigateur. Fais défiler jusqu'en bas.
Toutes les photos s'affichent ? Parfait.

S'il y a des cadres vides, c'est qu'une photo manque ou que son nom est
mal écrit. Corrige avant de continuer.

---

## Étape 2 — Créer le compte Netlify

1. Va sur **netlify.com**
2. Clique sur **Sign up**
3. Choisis « Email », mets ton adresse et un mot de passe
4. Tu reçois un mail, clique sur le lien dedans

C'est gratuit. Aucune carte bancaire demandée.

---

## Étape 3 — Déposer le site

1. Va sur **app.netlify.com/drop**
2. Tu vois un grand rectangle en pointillés
3. Attrape le dossier **`la-cantine-de-lea` en entier** avec ta souris et
   lâche-le dans le rectangle

Attention : le dossier entier, pas le fichier `index.html` tout seul,
pas le fichier zip.

Attends dix secondes. Une adresse apparaît, du genre
`brave-tourteau-4f2a.netlify.app`. Clique dessus : ton site est en ligne.

---

## Étape 4 — Rendre le site visible de tous

Par défaut Netlify garde le site privé.

Sur la page du site, cherche le bouton turquoise **Make public** et
clique dessus. Sans ça, les visiteurs tomberont sur une demande de
connexion.

---

## Étape 5 — Trouver ce qu'il faut recopier

Toujours dans Netlify :

1. Clique sur **Domain management** (ou Project configuration → Domains)
2. Clique sur **Add a domain**
3. Tape ton nom de domaine, par exemple `lacantinedelea.fr`, puis valide

Netlify affiche alors des informations à recopier. Ne ferme pas cette
page : garde-la ouverte dans un onglet.

Tu vas y lire deux choses :

- une **adresse IP**, une suite de chiffres comme `75.2.60.5`
- une **adresse en .netlify.app**, celle de ton site

---

## Étape 6 — Visser la plaque sur la porte

Ouvre un nouvel onglet et connecte-toi là où tu as acheté le domaine.

Cherche dans le menu : **Zone DNS**, ou **Gérer les DNS**,
ou **DNS records**. C'est le même endroit sous des noms différents.

Tu vas ajouter deux lignes.

**Première ligne**

| Case | Ce que tu écris |
|---|---|
| Type | `A` |
| Nom (ou Host) | `@` |
| Valeur (ou Cible) | l'adresse IP lue à l'étape 5 |

**Deuxième ligne**

| Case | Ce que tu écris |
|---|---|
| Type | `CNAME` |
| Nom (ou Host) | `www` |
| Valeur (ou Cible) | ton adresse en `.netlify.app` |

S'il y a une case « TTL », laisse ce qui est proposé.

Enregistre.

Le `@` veut dire « le domaine tout court », `lacantinedelea.fr`.
Le `www` sert à ceux qui tapent `www.lacantinedelea.fr`.

---

## Étape 7 — Attendre

Le changement met entre 10 minutes et quelques heures à se propager
partout dans le monde. C'est normal, il n'y a rien à faire.

Pendant ce temps, Netlify fabrique tout seul le petit cadenas HTTPS.
Dans Domain management, la ligne doit finir par afficher
**Netlify DNS ✓** ou **HTTPS ✓** en vert.

Tape ensuite ton adresse dans le navigateur. Le site s'affiche.

---

## Si quelque chose cloche

**Le site affiche « Page not found »**
Tu as déposé `index.html` seul au lieu du dossier. Recommence l'étape 3
avec le dossier entier.

**Les photos ne s'affichent pas en ligne mais marchaient chez toi**
Un nom de fichier a une majuscule quelque part. En ligne, `Hero.jpg` et
`hero.jpg` sont deux fichiers différents. Mets tout en minuscules.

**Le domaine affiche encore l'ancien site**
L'ancien site est peut-être encore branché dessus. Va dans ton ancien
hébergeur (WordPress par exemple) et retire le domaine de là-bas.

**Ça ne marche toujours pas après 24 heures**
Retourne dans la zone DNS. Vérifie qu'il n'y a pas une vieille ligne
de type `A` ou `CNAME` qui traîne avec le même nom. S'il y en a une,
supprime-la : deux plaques sur la même porte, ça ne marche pas.

---

## Un avertissement important

Si tu as une adresse mail qui finit par `@lacantinedelea.fr`, ne touche
qu'aux deux lignes décrites ici.

Ne clique jamais sur une proposition du style « changer les serveurs de
noms » ou « utiliser Netlify DNS ». Ça couperait ta boîte mail.

---

## Pour modifier le site plus tard

1. Change ce que tu veux dans `index.html`, ou remplace une photo
   dans `images/`
2. Retourne sur **app.netlify.com/drop**
3. Redépose le dossier entier

La nouvelle version remplace l'ancienne en quelques secondes.
Le nom de domaine, lui, reste branché : tu n'y retouches plus jamais.
