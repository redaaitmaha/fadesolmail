# FADESOL — Signature e-mail / Email signature

Reproduction HTML de la maquette « Frame 1 » (Souad SIFATE — Service Commercial),
construite à partir des fichiers sources du dossier (`20ANS LOGO.svg`, `LOGO.svg`,
`SLOGAN.svg`, `imagebg.svg`).

```
mail signature/
├── signature.html      ← la signature (tableau + styles en ligne, 573 × 295 px)
├── assets/
│   ├── header-visual.jpg   343 × 236  (visuel « 20 ans » + mosaïque métiers, 2x)
│   ├── footer-bar.png      573 × 44   (dégradé + logos, 2x)
│   ├── icon-email.png       13 × 13
│   ├── icon-phone.png       13 × 13
│   ├── icon-pin.png         13 × 13
│   └── icon-globe.png       13 × 13
├── 20ANS LOGO.svg / LOGO.svg / SLOGAN.svg / imagebg.svg   (sources, inchangés)
└── README.md
```

Ouvrez `signature.html` dans un navigateur pour voir le rendu.

## 1. Héberger les images (obligatoire avant l'envoi)

Les clients mail ne savent pas lire un chemin local : les images doivent être en ligne.

1. Uploadez le contenu de `assets/` sur le site, par exemple
   `https://www.fadesol.com/email/` (ou tout autre hébergement HTTPS public).
2. Dans `signature.html`, remplacez chaque `src="assets/…"` par l'URL complète, ex. :
   `src="https://www.fadesol.com/email/header-visual.jpg"`.
3. Vérifiez que les URL s'ouvrent bien dans un navigateur **avant** d'installer la signature.

## 2. Installer la signature

**Outlook (Windows)**
1. Ouvrez `signature.html` dans Chrome / Edge.
2. `Ctrl+A` puis `Ctrl+C`.
3. Outlook → Fichier → Options → Courrier → Signatures… → Nouveau, puis collez (`Ctrl+V`).
4. Enregistrez et choisissez la signature pour les nouveaux messages / réponses.

**Outlook Web / Microsoft 365** — Paramètres → Courrier → Rédiger et répondre → Signature → collez.

**Gmail** — Paramètres → Général → Signature → Créez-en une → collez, puis Enregistrer.

**Apple Mail** — Mail → Réglages → Signatures → créez une signature, collez le contenu.

## 3. Personnaliser

- Nom / fonction / coordonnées : texte réel (sélectionnable, cherchable), modifiable directement.
- Couleurs : bleu `#24377A`, vert `#007341`, texte `#313A50`.
- Police : `Montserrat` si installée, sinon `Segoe UI` / `Helvetica Neue` / `Arial`.
- Largeur totale 573 px : ne pas la dépasser (au-delà, la signature se coupe dans Outlook).
- Les visuels sont fournis en 2× (retina) : gardez les attributs `width` / `height`
  indiqués dans le HTML, ne les agrandissez pas.

## 4. Écarts assumés par rapport à la maquette

- Coordonnées en **9 px** au lieu de 8 px (lisibilité à l'écran) ; interlignes conservés.
- Lettres du nom et de la fonction légèrement resserrées (`letter-spacing`) pour retrouver
  la largeur de la maquette avec les polices système.
- Les libellés Figma (« Frame 1 », « 76.6 × 19.6 ») visibles sur le PNG de référence
  ne font pas partie du design et n'ont pas été repris.

## 5. Régénérer les images

Les visuels sont générés depuis les SVG sources (rendu net, transparence conservée).
En cas de modification des SVG, il suffit de re-exporter :

- `20ANS LOGO.svg` → 175 × 212 px, collé à (21, 68) sur le visuel d'en-tête ;
- `LOGO.svg` → 154 × 40 px, collé à (57, 24) sur le bandeau ;
- `SLOGAN.svg` → 138 × 58 px, collé à (978, 16) sur le bandeau ;
- `imagebg.svg` (mosaïque) → 634 × 452 px, collé à (29, 11) sur le visuel d'en-tête ;
- bandeau 1146 × 88 px, dégradé `#26367A` → `#017044`.
