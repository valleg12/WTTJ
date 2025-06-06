# Welcome to the Jungle - Documentation Technique et Utilisateur

## 1. Vue d'ensemble du projet

Welcome to the Jungle est une plateforme web immersive, conçue pour favoriser les interactions sociales et le retour au bureau dans un environnement ludique et engageant. La plateforme utilise un thème jungle/pixel-art et intègre des mascottes animales personnalisables pour représenter les collaborateurs.

### Fonctionnalités principales
- Interface immersive avec thème jungle/pixel-art
- Mascottes animales personnalisables
- Intégration avec Google Workspace et Slack
- Système de présence et d'activités
- Tableau de bord personnalisé
- Calendrier interactif
- Statistiques et analyses
- Notifications et alertes

## 2. Documentation Technique

### Prérequis
- Node.js (version 18 ou supérieure)
- npm (version 9 ou supérieure)
- Compte Google Workspace
- Compte Slack
- Compte Netlify (pour le déploiement)

### Installation

1. Cloner le dépôt :
```bash
git clone [URL_DU_REPO]
cd WelcomeToTheJungle-main
```

2. Installer les dépendances :
```bash
npm install
```

3. Configurer les variables d'environnement :
Créer un fichier `.env` à la racine du projet avec les variables suivantes :
```
VITE_GOOGLE_CLIENT_ID=votre_client_id
VITE_SLACK_CLIENT_ID=votre_client_id
VITE_DUST_API_KEY=votre_api_key
```

4. Lancer le serveur de développement :
```bash
npm run dev
```

### Architecture Technique

#### Stack Technologique
- Frontend : React + TypeScript
- UI : Tailwind CSS + shadcn-ui
- Build : Vite
- Déploiement : Netlify
- Intégrations : Google Workspace API, Slack API
- IA : Dust API pour la personnalisation

#### Structure du Projet
```
WelcomeToTheJungle-main/
├── src/
│   ├── components/     # Composants React
│   ├── hooks/         # Custom hooks
│   ├── pages/         # Pages de l'application
│   ├── services/      # Services et API
│   ├── styles/        # Styles globaux
│   └── utils/         # Utilitaires
├── public/            # Assets statiques
└── [fichiers de config]
```

### Déploiement et CI/CD
- Intégration continue avec Netlify
  - Déploiement automatique à chaque push sur la branche main
  - Prévisualisation des pull requests
  - Rollback automatique en cas d'erreur
  - Variables d'environnement sécurisées
  - Cache optimisé pour les assets statiques

### Intégrations

#### Google Workspace
- Synchronisation du calendrier
- Authentification
- Gestion des événements

#### Slack
- Bot pour les notifications
- Intégration des statuts
- Commandes slash
- Accès direct depuis Slack
- Notifications en temps réel des mises à jour
- Alertes de déploiement
- Rappels d'événements
- Suggestions personnalisées
- Commandes slash pour les actions rapides
- Statuts synchronisés avec la plateforme

#### Dust AI
Le système utilise Dust AI pour personnaliser les interactions avec les mascottes :
- Analyse des événements et habitudes
- Adaptation aux secteurs de travail
- Prise en compte des localisations
- Intégration des données Slack
- Suggestions personnalisées

## 3. Guide Utilisateur

### Pour les Collaborateurs

#### Création de Mascotte
1. Cliquer sur "Créer une mascotte"
2. Remplir le questionnaire d'onboarding :
   - Localisation
   - Jours préférés
   - Collaborateurs fréquents
   - Préférences de notifications
   - Choix de l'animal
   - Nom réel
   - Équipe

#### Utilisation Quotidienne
- Visualiser sa présence sur la carte
- Consulter les activités prévues
- Interagir avec les collègues
- Recevoir des suggestions personnalisées

### Pour les Managers

#### Tableau de Bord
- Vue d'ensemble de l'équipe
- Statistiques de présence
- Planification des activités
- Gestion des notifications

#### Fonctionnalités Spécifiques
- Création d'événements d'équipe
- Suivi des objectifs
- Rapports d'activité

### Pour les RH

#### Outils d'Administration
- Gestion des accès
- Configuration des règles
- Export des données
- Tableaux de bord analytiques

### Procédures d'Urgence

#### Extraction des Données
1. Accéder au panneau d'administration
2. Sélectionner "Export des données"
3. Choisir la période et le format
4. Télécharger le fichier

## 4. FAQ

### Questions Générales
Q: Comment accéder à la plateforme ?
R: Via le navigateur web ou directement depuis Slack.

Q: Comment modifier ma mascotte ?
R: Cliquer sur votre mascotte et utiliser le menu de personnalisation.

### Questions Techniques
Q: Que faire en cas de problème de connexion ?
R: Vérifier votre connexion internet et vos identifiants Google Workspace.

Q: Comment synchroniser mon calendrier ?
R: La synchronisation est automatique après l'authentification Google.

### Questions sur l'IA
Q: Comment Dust personnalise-t-il les interactions ?
R: L'IA analyse vos activités, localisation et interactions pour adapter les suggestions.

## 5. Support et Maintenance

### Contact
- Support technique : [email]
- Urgences : [numéro]

### Processus de Support
- Ticketing système intégré
- SLA définis
- Procédures d'escalade
- Base de connaissances
- Formation continue

### Maintenance et Documentation
- Documentation vivante
  - Mise à jour automatique via les commits
  - Versioning des changements
  - Historique des modifications
  - Guide de contribution
  - Standards de code
  - Procédures de déploiement

## 6. Ressources

### Assets et Ressources Graphiques
- Mascottes : `/public/mascots/`
- Arrière-plans : `/public/backgrounds/`
- Icônes : `/public/icons/`

### Dépendances Principales
- React 18+
- TypeScript 5+
- Tailwind CSS
- shadcn-ui
- Vite
- Google Workspace API
- Slack API
- Dust AI API

---
