<p align="center">
  <img src="docs/images/chatbot_fr.png"
       alt="Chatbot conversation interface — example of a local Flask chatbot in use"
       width="1200">
</p>

> 🇫🇷 Français | [🇬🇧 English](./README.md)

![License](https://img.shields.io/badge/License-LICENSE.md-lightgreen.svg)
![OpenAI Optional](https://img.shields.io/badge/OpenAI-Optional-412991.svg)
![Flask](https://img.shields.io/badge/Framework-Flask-000000?style=flat)
![Offline First](https://img.shields.io/badge/Mode-Offline%20First-0095b1?style=flat)
[![Flask Chatbot](https://img.shields.io/badge/Flask%20Chatbot-0095b1?style=flat)](https://palks-studio.com/fr/chatbot-flask)

<p align="center">
  <a href="https://palks-studio.com">
    <img src="https://img.shields.io/badge/Palks%20Studio-Website-0095b1?style=for-the-badge" />
  </a>
</p>

# Chatbot Flask Avance — Version 2.0

> Ce dépôt constitue une présentation technique et une documentation du projet.  
> Il ne contient pas de code source téléchargeable ni de fichiers de production.

Un projet complet pour créer ton propre **assistant conversationnel avec Flask**, prêt à être utilisé :  

- **en local (localhost)**  
- **sur un hébergement mutualisé comme o2switch (Passenger / cPanel)**

Aucune base externe, aucune dépendance cachée. Tu peux l’utiliser tel quel, le modifier ou l’intégrer dans un autre site ou une API.

[![Flask Chatbot](https://img.shields.io/badge/Flask%20Chatbot-0095b1?style=flat)](https://palks-studio.com/fr/chatbot-flask)

---

## Vue d’ensemble

Ce projet propose un assistant conversationnel auto-hébergé, structuré et basé sur Flask,  
conçu pour les développeurs et les équipes souhaitant garder un contrôle total sur  
le comportement et le déploiement de leur chatbot.

L’architecture privilégie :  

- une base de connaissances locale (JSON) prioritaire  
- un comportement prévisible en environnement professionnel  
- une intégration IA optionnelle (OpenAI)  
- un déploiement simple, sans dépendance à une plateforme SaaS externe

---

## Structure du projet

```
chatbot_flask_avance_2.0/
│
├── core/                     → Logique du chatbot et traitement des requêtes
├── interface/                → Interface utilisateur (chat et widget)
├── storage/                  → Couche de persistance optionnelle
├── config/                   → Configuration de l’environnement et dépendances
├── deployment/               → Déploiement (hébergement et conteneurisation)
├── data/                     → Base de connaissances d’exemple
├── logs/                     → Suivi et journalisation des erreurs
│
└── docs/
    ├── INSTALL.md            → Guide utilisateur complet
    ├── README_TECHNIQUE.md   → Documentation principale du projet
    ├── README.md             → Documentation et guides du projet
    └── CUSTOMISATION.md      → Personnalisation du bot (design, réponses, OpenAI…)
```


---

## Points forts

- **Compatible o2switch / Passenger (hébergement mutualisé)**  
- **Aucune base de données requise** (fichier JSON seulement)  
- **Code lisible, commenté, facilement personnalisable**  
- **CORS activé : utilisable avec un site web ou une interface front-end**  
- **Système de logs intégré :** erreurs enregistrées automatiquement dans le dossier `/logs/`

---

## Cas d’usage typiques

Ce chatbot est conçu pour :  

- assistants internes de connaissances  
- automatisation de support ou de documentation  
- assistants IA auto-hébergés  
- outils internes nécessitant des réponses contrôlées  
- sites web intégrant un widget conversationnel

Le système peut fonctionner entièrement hors ligne à partir d’une base de connaissances locale,  
ou utiliser OpenAI de manière optionnelle lorsque des réponses étendues sont nécessaires.

---

## Fichiers générés automatiquement

Lorsque le chatbot est lancé pour la première fois, certains fichiers sont créés automatiquement :  

| Fichier                 | Rôle                                                                            |
|-------------------------|---------------------------------------------------------------------------------|
| Fichier de persistance  | Peut être généré pour stocker les conversations si la persistance est activée   |
| `logs/errors.log`       | Créé uniquement en cas d’erreur serveur                                         |
| Fichier d’environnement | À créer à partir du modèle fourni pour activer les fonctionnalités optionnelles |

---

## Modes de fonctionnement

| Mode                        | Description                                        | Nécessite une clé OpenAI |
|-----------------------------|----------------------------------------------------|--------------------------|
| **Local JSON** (par défaut) | Réponses générées depuis la base locale            | Non                      |
| **OpenAI GPT (optionnel)**  | Utilisation de l’API OpenAI si une clé est fournie | Oui                      |

Le mode est automatiquement sélectionné en fonction de la présence d’une configuration d’API dans l’environnement.  
Aucune consommation de tokens si aucune clé n'est renseignée.

---

## Journaux d’erreurs (Logs)

Le dossier `logs/` permet d’enregistrer automatiquement les erreurs du serveur Flask :  

- création automatique des fichiers de journalisation en cas d’erreur  
- génération automatique du dossier `logs/` si nécessaire  
- enregistrement de la date, du message et de la trace complète (`traceback`)

Ce système fonctionne :  

- en mode local  
- avec ou sans OpenAI  
- en production (Passenger / hébergement mutualisé)

---

**Palks Studio — Version 2.0 (Édition Avancée)**  
Compatible avec Python 3.12+ et Flask 3.0+

© Palks Studio — voir LICENSE.md  
- https://palks-studio.com
