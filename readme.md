# Jungle Gather (WTTJ)

## Présentation

**Jungle Gather** est une application web immersive inspirée de Gather, conçue pour favoriser la dynamique sociale et la gestion du planning dans une entreprise multi-sites. L'interface propose un univers pixel-art, un calendrier interactif, la gestion de la présence (remote/préso), des avatars animaux (mascottes) et des fonctionnalités d'export de listes (présents, remote).

## Fonctionnalités principales

- **Calendrier interactif** :
  - Vue semaine, mini-calendrier, création d'événements dynamiques
  - Pastilles de présence (présentiel/remote/aucun) sous chaque jour
  - Légende explicative et code couleur
- **Gestion de la présence** :
  - Sélection cyclique remote/préso/aucun pour chaque jour
  - Export CSV de la liste des personnes en remote ou en présentiel
- **Avatars mascottes** :
  - Chaque utilisateur est représenté par un animal sur la carte
  - Visualisation en temps réel des collègues présents
- **Sidebar et navigation** :
  - Accès rapide au calendrier, à la liste des événements, et à l'export
- **Modale de création d'événement** :
  - Formulaire complet (titre, date, heure, lieu, description)
  - Ajout dynamique dans le calendrier
- **UI moderne et responsive** :
  - Design inspiré Notion/Linear/Slack, animations douces, mobile friendly

## Architecture du projet

```
jungle-wanderer-paradise/
├── src/
│   ├── components/
│   │   ├── CalendarView.tsx         # Vue principale calendrier et gestion événements
│   │   ├── GameMap.tsx             # Carte principale avec mascottes et remote
│   │   ├── SidebarDashboard.tsx    # Sidebar navigation (calendrier, export...)
│   │   ├── ...                     # Autres composants UI (onboarding, avatars...)
│   │   └── ...
│   ├── context/
│   │   └── GameContext.tsx         # Contexte global (utilisateurs, présence...)
│   └── index.css                   # Styles globaux
├── readme.md                       # Ce fichier
├── package.json                    # Dépendances et scripts
└── ...
```

## Installation & Lancement

1. **Cloner le repo**
   ```bash
   git clone https://github.com/valleg12/WTTJ.git
   cd WTTJ
   ```
2. **Installer les dépendances**
   ```bash
   npm install
   # ou
   yarn install
   ```
3. **Lancer le projet en développement**
   ```bash
   npm run dev
   # ou
   yarn dev
   ```
4. **Accéder à l'application**
   Ouvrir [http://localhost:3000](http://localhost:3000) dans votre navigateur.

## Crédits & Liens utiles

- Développé par Victorien Allegre et collaborateurs.
- UI inspirée de Gather, Notion, Linear.
- [Repo GitHub](https://github.com/valleg12/WTTJ)

---

Pour toute question ou contribution, ouvrez une issue ou contactez l'auteur sur GitHub.
