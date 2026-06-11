# CLAUDE.md — demos-tpe-88

Repo **public** de maquettes de sites web statiques, réalisées à notre initiative à des fins de
démonstration commerciale, **non contractuelles**. Déploiement : GitHub Pages (`main`, racine).
Chaque maquette est consultée **sur mobile, en 4G moyenne** : la performance prime sur toute
sophistication. Simple et impeccable bat riche et fragile.

## Source de vérité

`docs/CDC-maquettes.md` est le cahier des charges local **non versionné** (le dossier `docs/`
est exclu par `.gitignore` et ne doit jamais entrer dans l'historique git). En cas de conflit
entre ce fichier et le CDC, **le CDC gagne**. Le lire en entier avant de produire ou modifier
une maquette.

## Règles techniques (toutes les maquettes)

- Un dossier par maquette : `/<slug>/index.html`, CSS/JS **inline**, images locales dans `/<slug>/img/`.
- HTML/CSS/JS vanilla, statique, single-page (+ ancres). Zéro framework, zéro build, zéro tracking, zéro cookie.
- 2 Google Fonts max par maquette (`display=swap`), icônes en SVG inline.
- Budgets : poids page < 1,5 Mo · LCP < 2 s · contraste AA · aucune ressource bloquante.
- `<meta name="robots" content="noindex">` sur chaque page (en plus du `robots.txt` racine).
- Images : **libres de droits uniquement** (Unsplash/Pexels), téléchargées en local, ≤ 1600 px,
  WebP qualité ~75, ≤ 200 Ko chacune, 3 à 5 par maquette. Si téléchargement impossible :
  placeholders SVG élégants + commentaire `TODO`.
- Bandeau légal fixe en pied de viewport sur chaque page (texte exact dans le CDC).
- Numéros de téléphone cliquables (`tel:`), adresse liée vers Google Maps, JSON-LD schema.org
  `LocalBusiness`/`Restaurant` avec les NAP réels (nom, adresse, téléphone, horaires).
- SEO local pré-rempli : `title` et meta description orientés « métier + Rambervillers ».
- Modules commande / réservation / devis : **simulés côté front** (localStorage autorisé),
  aboutissant à un écran « Ceci est une démonstration ». Rien de branché : ni backend,
  ni paiement, ni collecte de données.
- Prix et contenus d'exemple : crédibles, marqués `[À REMPLACER]` en **commentaire HTML**
  (invisible à l'écran).

## Design

- Chaque maquette suit la direction de sa fiche du CDC : palette, typographie, ton,
  fonctionnalité phare propre à la cible.
- **Interdiction de livrer plusieurs fois le même template recoloré** : le squelette technique
  peut être partagé, l'identité visuelle non. Objectif : que le commerçant pense
  « c'est déjà mon site ».
- Mobile-first : concevoir et vérifier en 390 px d'abord, puis 1440 px.

## Workflow

- Budget : ≤ 1 h équivalent par maquette.
- Par maquette : lire la fiche du CDC → construire → autocontrôle avec la checklist
  « Definition of done » du CDC → servir en local (`python3 -m http.server`) et vérifier le
  rendu en 390 px puis 1440 px → commit `feat(<slug>): maquette v1` → ajouter la ligne
  (maquette, URL, statut) au tableau du README.
- `git add` **explicite uniquement** (jamais `git add -A` ni `git add .`) : le dossier `docs/`
  ne doit jamais être ajouté, même par accident.
- Vérifier avant tout premier add que `git check-ignore docs/` répond, et après coup que
  `git log --all --stat` ne montre aucun fichier de `docs/`.
- En cas d'ambiguïté non bloquante : trancher et noter la décision dans le message de commit.

## Interdits

- Committer quoi que ce soit du dossier `docs/`, ou recopier son contenu d'analyse
  (lectures commerciales, contexte des établissements) dans un fichier versionné, un message
  de commit ou le README. Seules les **données factuelles publiques** (nom, adresse, téléphone,
  horaires, note Google, courts extraits d'avis) peuvent apparaître dans les maquettes.
- Photos issues des fiches Google/Facebook ou des sites des établissements : **jamais**
  (droit d'auteur). Libres de droits uniquement.
- Framework, build, CDN de librairies, tracking, cookies, backend, paiement réel.
- Dénigrer l'existant d'un établissement dans le contenu d'une maquette.
