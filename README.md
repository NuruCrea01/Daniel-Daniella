# Invitation de mariage – Daniel & Daniella

Site d’invitation en une seule page (HTML, CSS, JavaScript), sans installation ni outil de build. Il est prêt à être hébergé gratuitement sur Vercel ou Netlify.

## Contenu du dossier

```
site-mariage/
├── index.html      → tout le site (textes, styles, animations)
├── photos/         → les images du site (à remplacer par les vôtres)
│   ├── accueil.jpg → photo plein écran de la page d’accueil
│   └── photo1.jpg … photo6.jpg → galerie
└── README.md
```

## Modifier les textes

Ouvrez `index.html` avec un éditeur de texte (Bloc-notes, VS Code…). Tout en haut, le bloc **« TEXTES À MODIFIER ICI »** contient :

| Clé | Rôle |
|---|---|
| `dateISO` | Date et heure du compte à rebours, au format `AAAA-MM-JJTHH:MM:SS` |
| `dateTexte` | Date affichée sur la page |
| `accroche`, `accueil` | Phrases d’accueil |
| `histoire` | Les 3 étapes de la frise (rencontre, premier rendez-vous, demande) |
| `programme` | Les horaires et moments de la journée |
| `lieuNom`, `adresse`, `ville` | Lieu, utilisé aussi pour la carte et l’itinéraire |
| `dressCode`, `couleurs` | Dress code et pastilles de couleur |
| `dateLimite` | Date limite de réponse |
| `whatsapp` | Numéro WhatsApp avec indicatif, sans « + » ni espaces (ex. `243812345678`) |
| `messageWhatsapp` | Message pré-rempli envoyé par l’invité |
| `hashtag` | Hashtag du pied de page |

> **À faire en priorité :** la date `2012-12-12` est passée, donc le compte à rebours affiche 00. Mettez la vraie date dans `dateISO`, `dateTexte` et `dateLimite`. Remplacez aussi le numéro WhatsApp fictif.

## Remplacer les photos

1. Préparez vos photos en JPG, de 1 à 2 Mo maximum chacune (le site reste plus rapide).
2. Donnez-leur **exactement** les noms ci-dessus (`accueil.jpg`, `photo1.jpg` … `photo6.jpg`).
3. Copiez-les dans le dossier `photos/` en remplaçant les images temporaires.

Pour utiliser d’autres noms de fichiers, modifiez `photoAccueil` et `galerie` dans le bloc de textes.

## Couleurs et polices

- Couleurs : crème `#f6eee0`, terracotta `#b9583a`, brun profond `#3a2318` (variables `--cr`, `--tc`, `--br` au début du CSS).
- Polices (Google Fonts) : Pinyon Script (prénoms), Bodoni Moda (titres), Cinzel (petits intertitres), Jost (textes).

## Animations

Les apparitions et les transitions sont lentes et discrètes. Elles sont automatiquement désactivées si l’appareil demande de réduire les animations (réglage d’accessibilité sur iPhone et Android).

## Tester sur votre ordinateur

Double-cliquez sur `index.html` : le site s’ouvre dans le navigateur. La carte Google Maps et les polices demandent une connexion internet.

## Mettre en ligne (Vercel)

1. Créez un compte sur [github.com](https://github.com) et un dépôt public (par exemple `mariage-daniel-daniella`).
2. Envoyez-y `index.html` et le dossier `photos` (via « uploading an existing file »). `index.html` doit être à la racine du dépôt.
3. Créez un compte sur [vercel.com](https://vercel.com) avec « Continue with GitHub ».
4. Cliquez sur « Add New… » puis « Project », choisissez votre dépôt et cliquez sur « Import ».
5. Laissez les réglages par défaut (Framework Preset : Other) et cliquez sur « Deploy ».
6. Copiez le lien obtenu (`xxx.vercel.app`) et partagez-le avec vos invités.

Pour modifier le site ensuite : ouvrez le fichier dans GitHub, cliquez sur le crayon, modifiez, puis « Commit changes ». Vercel republie automatiquement.

**Netlify** fonctionne aussi : sur [app.netlify.com/drop](https://app.netlify.com/drop), glissez-déposez le dossier `site-mariage` pour obtenir un lien immédiatement.
