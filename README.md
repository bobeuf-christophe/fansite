# We are fans 🎬

> Trois fans, trois passions, un seul site.

**We are fans** est un site vitrine statique (HTML / CSS) réalisé à plusieurs mains. Chaque membre de l'équipe y présente l'univers qu'il adore :

| Fan | Univers | Ce que vous y trouverez |
|-----|---------|-------------------------|
| Fan n°1 | **Les Simpson** | Présentation de la famille de Springfield et une galerie photos |
| Fan n°2 | **Perceval (Kaamelott)** | La légende du chevalier, les jeux du pays de Galles (Pélican, Sirop, Sloubi…) et un bouton « C'est pas faux ! » sonore |
| Fan n°3 | **Les Shadoks** | L'histoire des Shadoks, une timeline des saisons et les épisodes pilotes à regarder |

Une page **Contact** permet aussi aux visiteurs de s'inscrire et d'indiquer leur univers préféré.

---

## 🚀 Lancer le site

Aucun outil ni dépendance n'est nécessaire : le site est 100 % statique.

```bash
git clone https://github.com/bobeuf-christophe/fansite.git
cd fansite
```

Ouvrez ensuite `index.html` dans votre navigateur.

Pour profiter correctement des vidéos et de l'audio, vous pouvez aussi lancer un petit serveur local :

```bash
# avec Python
python3 -m http.server 8000
# puis ouvrir http://localhost:8000
```

Ou utiliser l'extension **Live Server** de VS Code.

> ℹ️ Le dépôt pèse environ 120 Mo à cause des vidéos des Shadoks : le clonage peut prendre un peu de temps.

---

## 📁 Structure du projet

```
fansite/
├── index.html              # Page d'accueil (présentation des 3 univers)
├── css/
│   ├── styles.css          # Styles communs (header, navigation, footer)
│   ├── accueil.css         # Styles de la page d'accueil
│   └── formulaire.css      # Styles du formulaire de contact
├── pages/
│   └── formulaire.html     # Formulaire de contact / inscription
├── page-fan1/              # 🍩 Les Simpson
│   ├── fansite1.html       # Présentation des personnages
│   ├── galerie.html        # Galerie photos
│   ├── fansite1.css
│   ├── galerie.css
│   └── images/
├── page-fan2/              # ⚔️ Perceval (Kaamelott)
│   ├── fansite2.html       # Légende de Perceval et jeux gallois
│   ├── fansite2.css
│   ├── cpafo.mp3           # Le fameux « C'est pas faux ! »
│   ├── audio/generique.mp3
│   └── images/
└── page-fan3/              # 🪣 Les Shadoks
    ├── fansite3.html       # Présentation des Shadoks
    ├── events.html         # Timeline des 4 saisons
    ├── watch-s1.html … watch-s4.html   # Épisodes pilotes par saison
    ├── watch-s*.mp4        # Vidéos (saisons 1, 2 et 4)
    ├── fansite3.css
    └── images (.webp / .jpg)
```

---

## ✨ Fonctionnalités

- **Navigation commune** sur toutes les pages : Home · Les Simpson · Perceval · Les Shadoks · Contact us
- **Galerie photos** des Simpson
- **Bouton sonore** « C'est pas faux ! » sur la page Perceval
- **Lecteur vidéo HTML5** pour les pilotes des Shadoks (archives INA, en français) ; la saison 3 renvoie vers YouTube
- **Timeline** des quatre saisons des Shadoks
- **Formulaire de contact** avec validation HTML native : champs obligatoires, code postal à 5 chiffres, e-mail et téléphone, choix de l'univers préféré
- **Liens vers les réseaux sociaux** depuis l'accueil

---

## 🛠️ Technologies

- **HTML5** (balises sémantiques, `<audio>`, `<video>`, formulaires)
- **CSS3** (une feuille commune + une feuille par univers)
- **Google Fonts** : Bangers, Cinzel Decorative, IM Fell English
- Aucun framework, aucune étape de build

---

## 🤝 Contribuer

Chaque fan travaille sur sa propre branche puis ouvre une Pull Request vers `main` :

```bash
git checkout -b ma-branche
# ... modifications ...
git add .
git commit -m "Description de la modification"
git push origin ma-branche
```

Quelques règles pour garder le site cohérent :

- Gardez le **header** et le **footer** identiques sur toutes les pages
- Placez vos fichiers dans **votre dossier** `page-fanX/`
- Utilisez des **chemins relatifs** (`../index.html`, `images/…`)
- Pensez à remplir l'attribut `alt` de vos images

---

## ⚠️ Mentions

Projet de fans, réalisé dans un cadre pédagogique et sans but commercial.
*Les Simpson* © Matt Groening / 20th Television · *Kaamelott* © Alexandre Astier · *Les Shadoks* © Jacques Rouxel / INA.
Les images, sons et vidéos restent la propriété de leurs ayants droit respectifs.
