# Jungle Gather (WTTJ)

**Jungle Gather** est une interface web immersive inspirée de Gather, conçue pour dynamiser la vie d'équipe, la gestion de planning et la présence dans une entreprise multi-sites, le tout dans un univers pixel-art ludique.

---

## 🚀 Fonctionnalités principales

- **Calendrier interactif** : double agenda (événements, planning personnel), navigation semaine/mois, responsive, francisé.
- **Déclaration de présence** : sélection simple (présentiel, remote, aucun) pour chaque jour, pastilles synchronisées.
- **Création d'événements** : modale ergonomique, ajout dynamique, affichage dans la grille centrale.
- **Export CSV** : export des listes de présents/remote/participants en un clic (toujours accessible).
- **Vue "Events"** : accès rapide à tous les événements créés.
- **UI pixel-art** : avatars animaux, map immersive, sidebar moderne.
- **Accessibilité mobile** : design responsive, lisible sur tous supports.

---

## 🗂️ Architecture du projet

```
jungle-wanderer-paradise/
├── src/
│   ├── components/
│   │   ├── CalendarView.tsx         # Vue calendrier principale (logique, UI, modale)
│   │   ├── GameMap.tsx              # Carte pixel-art, mascottes, remote
│   │   ├── SidebarDashboard.tsx     # Sidebar navigation principale
│   │   ├── ...
│   ├── context/
│   │   └── GameContext.tsx          # Contexte global (utilisateurs, présence, etc.)
│   └── ...
├── public/
│   └── assets/                      # Images, avatars, backgrounds
├── package.json
└── readme.md
```

---

## ⚙️ Lancement rapide

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
3. **Lancer le projet**
   ```bash
   npm run dev
   # ou
   yarn dev
   ```
4. **Accéder à l'interface**
   - Ouvre [http://localhost:3000](http://localhost:3000) dans ton navigateur.

---

## 🛠️ Technologies utilisées
- **React** + **TypeScript**
- **Tailwind CSS** (UI moderne, responsive)
- **date-fns** (gestion des dates, francisation)
- **Lucide Icons** (icônes modernes)

---

## �� Points d'extension possibles
- Intégration Google Calendar / Slack / SSO
- Système de notifications et d'animations sociales
- Gestion fine des droits (admin, équipe, etc.)
- Drag & drop d'événements, avatars custom
- Statistiques de présence, suggestions sociales

---

## 📂 Repo GitHub
[https://github.com/valleg12/WTTJ](https://github.com/valleg12/WTTJ)

---

**Conçu pour une expérience collaborative, fun et efficace !**