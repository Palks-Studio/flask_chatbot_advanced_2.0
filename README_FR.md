# Flask Chatbot – Template Professionnel Avance (Version 2.0)

Un projet complet pour créer ton propre **assistant conversationnel avec Flask**, prêt à être utilisé :
- **en local (localhost)**
- **sur un hébergement mutualisé comme o2switch (Passenger / cPanel)**

Aucune base externe, aucune dépendance cachée. Tu peux l’utiliser tel quel, le modifier ou l’intégrer dans un autre site / API.

---

## Structure (Version publique)

```
Flask_Chatbot_Avance_2.0/ (Version Lite)
│
├── README_FR.md                   ← Documentation principale (publique)
├── LICENCE.txt                    ← Licence propriétaire (Palks Studio)
├── CUSTOMISATION.md               ← Guide et explications de personnalisation
├── requirements.txt               ← Dépendances Python principales
├── .env.example                   ← Exemple de configuration de l’API
│
├── version_publique/
│   ├── exemple_structure.txt      ← Aperçu complet de l’arborescence du projet (sans code)
│
└── docs/
    ├── images/
    │   └── Palks_Studio.png       ← Logo Palks Studio
```


*Cette arborescence est présentée à titre informatif.*

**⚠ Important**
Ce dépôt GitHub n’est qu’un aperçu partiel du projet.
Le fichier `README.md` représente uniquement une petite partie de la documentation complète.

La version commerciale inclut :
- le code source complet (Python, HTML, JSON, scripts)
- toute la documentation (INSTALL.md, README_TECHNIQUE.md, exemples, prompts, personnalisation avancée…)
- les fichiers générés automatiquement (`.env`, `data.db`, mémoire IA, etc.)

Le code complet est disponible uniquement dans la **version commerciale sous licence**.

---

## Points forts

- **Compatible o2switch / Passenger (hébergement mutualisé)**
- **Aucune base de données requise** (fichier JSON seulement)
- **Code lisible, commenté, facilement personnalisable**
- **CORS activé : utilisable avec un site web ou une interface front-end**
- **Système de logs intégré :** erreurs enregistrées automatiquement dans le dossier `/logs/`

---

## Fichiers générés automatiquement

Lorsque vous lancez le chatbot pour la première fois, certains fichiers sont créés automatiquement :

| Fichier        | Rôle                                           |
|----------------|-------------------------------------------------|
| `data.db`      | Base SQLite qui enregistre les conversations (se crée seule si `ENABLE_PERSISTENCE=true`) |
| `logs/errors.log` | Se crée uniquement si une erreur serveur survient |
| `.env`         | Doit être créé manuellement à partir de `.env.example` si vous souhaitez activer OpenAI |

⚠ **Ces fichiers ne sont pas inclus dans l’archive du projet.**

---

## Modes de fonctionnement

| Mode         | Description                                              | Nécessite une clé OpenAI |
|--------------|----------------------------------------------------------|---------------------------|
| **Local JSON** (par défaut) | Les réponses sont générées à partir du fichier `sample_data.json` | Non |
| **OpenAI GPT (optionnel)**  | En utilisant l'API ChatGPT si une clé est fournie dans `.env`     | Oui |

Le choix se fait automatiquement selon la présence de la variable `OPENAI_API_KEY` dans `.env`.  
Aucune consommation de tokens si aucune clé n'est renseignée.

---

## Journaux d’erreurs (Logs)

Le dossier `logs/` permet d’enregistrer automatiquement les erreurs du serveur Flask.
- Le fichier `logs/errors.log` est créé automatiquement si une erreur survient.
- Le dossier `logs/` est généré s’il n’existe pas (pas besoin de le créer manuellement).
- Chaque erreur contient :
- la date et l’heure
- le message d’erreur
- la trace complète (`traceback`) pour faciliter le débogage

Ce système fonctionne aussi bien :
- en mode local
- avec ou sans OpenAI
- en production (Passenger / hébergement mutualisé)

---

**Note**
Ce dépôt GitHub présente la structure et les fonctionnalités du projet.
Il ne contient pas l’intégralité du code source exécutable, des prompts, ni des fichiers sensibles (`.env`, `data.db`, mémoire IA...).
La version complète est disponible via la licence commerciale.

**Version complète du projet disponible ici**
https://ko-fi.com/palksstudio  
http://palks-studio.itch.io/  
https://palks.gumroad.com/

---

## Crédits et licences

Ce pack est une création originale de **Palks Studio**.
Toute revente, diffusion ou modification publique sans autorisation est interdite.
Usage personnel et professionnel autorisé.

---

**Palks Studio**
Créateur d’outils utiles et autonomes : scripts, templates et bases prêtes à l’emploi.
Simplicité, clarté, efficacité.

GitHub: https://github.com/Palks-Studio  
Gumroad: https://palks.gumroad.com/  
Discord: https://discord.gg/kzrSyThyZ7  
Twitter (X): https://x.com/PalksStudio  
Itch.io: http://palks-studio.itch.io/  
Ko-Fi: https://ko-fi.com/palksstudio

---

## Signature

_Créé par **Palks Studio** — Version 2.0 (édition avancée)_
_Compatible Python 3.12+ / Flask 3.0+_
