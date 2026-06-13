# demos-tpe-88

Maquettes statiques de démonstration, non contractuelles. Déploiement : GitHub Pages (`main`, racine).
Racine du site : page de présentation (placeholders contact/SIRET à compléter, `noindex` en attendant).

## Lot 1 — Rambervillers

| Maquette | URL | Statut |
| --- | --- | --- |
| ali-baba | https://lumenbot.github.io/demos-tpe-88/ali-baba/ | v1 · DoD ✓ |
| snack-de-la-place | https://lumenbot.github.io/demos-tpe-88/snack-de-la-place/ | v1 · DoD ✓ |
| coppia | https://lumenbot.github.io/demos-tpe-88/coppia/ | v1 · DoD ✓ |
| schwartz | https://lumenbot.github.io/demos-tpe-88/schwartz/ | v1 · DoD ✓ |
| dms | https://lumenbot.github.io/demos-tpe-88/dms/ | v1 · DoD ✓ |
| palomino | https://lumenbot.github.io/demos-tpe-88/palomino/ | v1 · DoD ✓ |
| pierron | https://lumenbot.github.io/demos-tpe-88/pierron/ | v1 · DoD ✓ |

## Lot 2 — Épinal

| Maquette | URL | Statut |
| --- | --- | --- |
| akdeniz | https://lumenbot.github.io/demos-tpe-88/akdeniz/ | v1 · DoD ✓ |
| casa-familia | https://lumenbot.github.io/demos-tpe-88/casa-familia/ | v1 · DoD ✓ |
| ws-electricite | https://lumenbot.github.io/demos-tpe-88/ws-electricite/ | v1 · DoD ✓ |
| ctoutfaire | https://lumenbot.github.io/demos-tpe-88/ctoutfaire/ | v1 · DoD ✓ |
| 1001-jardins | https://lumenbot.github.io/demos-tpe-88/1001-jardins/ | v1 · DoD ✓ |
| lattemann | https://lumenbot.github.io/demos-tpe-88/lattemann/ | v1 · DoD ✓ |
| lamielle | https://lumenbot.github.io/demos-tpe-88/lamielle/ | v1 · DoD ✓ |
| les-bulles | https://lumenbot.github.io/demos-tpe-88/les-bulles/ | v1 · DoD ✓ |

## Lot 3 — Saint-Dié / Raon

| Maquette | URL | Statut |
| --- | --- | --- |
| il-forno | https://lumenbot.github.io/demos-tpe-88/il-forno/ | v1 · DoD ✓ |
| tms-services | https://lumenbot.github.io/demos-tpe-88/tms-services/ | v1 · DoD ✓ |
| kebaberie-saint-martin | https://lumenbot.github.io/demos-tpe-88/kebaberie-saint-martin/ | v1 · DoD ✓ |
| chez-dom | https://lumenbot.github.io/demos-tpe-88/chez-dom/ | v1 · DoD ✓ |
| dolce-vita | https://lumenbot.github.io/demos-tpe-88/dolce-vita/ | v1 · DoD ✓ |
| bella-vita | https://lumenbot.github.io/demos-tpe-88/bella-vita/ | v1 · DoD ✓ |
| chocolats-carl | https://lumenbot.github.io/demos-tpe-88/chocolats-carl/ | v1 · DoD ✓ |
| renovon | https://lumenbot.github.io/demos-tpe-88/renovon/ | v1 · DoD ✓ |

## Développement

- Règles complètes : voir `CLAUDE.md` (source de vérité locale non versionnée : `docs/`).
- Servir en local : `python3 -m http.server` à la racine, vérifier en 390 px puis 1440 px.
- DoD par maquette : rendu 390/1440 px sans scroll horizontal, NAP réels exacts (`tel:`, lien Maps,
  horaires, JSON-LD), module phare simulé fonctionnel, bandeau légal + `noindex`, poids < 1,5 Mo,
  aucune ressource bloquante.
- Git : `git add` explicite uniquement (jamais `-A` ni `.`), `docs/` jamais versionné,
  contrôle `git log --all --stat` avant tout push.
