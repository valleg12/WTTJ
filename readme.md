/src
  /components
    /layout
      SidebarDashboard.tsx
      Topbar.tsx
      MainPanel.tsx
      SocialSidebar.tsx
    /dashboard
      DashboardView.tsx
      WeeklySummaryCard.tsx
      QuickActions.tsx
      SocialSuggestions.tsx
      ActivityFeed.tsx
    /calendar
      CalendarView.tsx
      CalendarGrid.tsx
      CalendarPopup.tsx
      WeekCopyButton.tsx
    /stats
      StatsView.tsx
      PieChart.tsx
      StackedBarChart.tsx
      TeamComparisonCurve.tsx
      PresenceHeatmap.tsx
      StatsFilters.tsx
      ExportButtons.tsx
    /hours
      HoursView.tsx
      HoursTable.tsx
      HoursDragDrop.tsx
      RecurringRules.tsx
      OvertimeAlert.tsx
    /preferences
      PreferencesView.tsx
      ProfileForm.tsx
      NotificationSettings.tsx
      DisplaySettings.tsx
      InterestSelector.tsx
    /shared
      UserAvatar.tsx
      ColleagueList.tsx
      ActivityCard.tsx
      LoadingSpinner.tsx
      AnimatedTransition.tsx
  /context
    UserContext.tsx
    CalendarContext.tsx
    StatsContext.tsx
    HoursContext.tsx
    PreferencesContext.tsx
    ActivitiesContext.tsx
  /hooks
    useUser.ts
    useCalendar.ts
    useStats.ts
    useHours.ts
    usePreferences.ts
    useActivities.ts
  /lib
    api.ts
    slackBot.ts
    dustIntegration.ts
    googleCalendar.ts
    utils.ts
  /assets
    /icons
    /images
  /styles
    tailwind.css
    theme.ts
  App.tsx
  main.tsx

  Voici une **architecture de projet hyper poussée** basée sur toutes tes notes et besoins, pensée pour un déploiement professionnel, évolutif et collaboratif.  
Cette structure te servira de roadmap : tu pourras cocher ce qui est fait, prioriser, et revenir dessus à tout moment.

---

# 🌴 Architecture fonctionnelle & technique — Jungle WorkFlow

## 1. Structure générale du projet

```
/src
  /components
    /layout
      SidebarDashboard.tsx
      Topbar.tsx
      MainPanel.tsx
      SocialSidebar.tsx
    /dashboard
      DashboardView.tsx
      WeeklySummaryCard.tsx
      QuickActions.tsx
      SocialSuggestions.tsx
      ActivityFeed.tsx
    /calendar
      CalendarView.tsx
      CalendarGrid.tsx
      CalendarPopup.tsx
      WeekCopyButton.tsx
    /stats
      StatsView.tsx
      PieChart.tsx
      StackedBarChart.tsx
      TeamComparisonCurve.tsx
      PresenceHeatmap.tsx
      StatsFilters.tsx
      ExportButtons.tsx
    /hours
      HoursView.tsx
      HoursTable.tsx
      HoursDragDrop.tsx
      RecurringRules.tsx
      OvertimeAlert.tsx
    /preferences
      PreferencesView.tsx
      ProfileForm.tsx
      NotificationSettings.tsx
      DisplaySettings.tsx
      InterestSelector.tsx
    /shared
      UserAvatar.tsx
      ColleagueList.tsx
      ActivityCard.tsx
      LoadingSpinner.tsx
      AnimatedTransition.tsx
  /context
    UserContext.tsx
    CalendarContext.tsx
    StatsContext.tsx
    HoursContext.tsx
    PreferencesContext.tsx
    ActivitiesContext.tsx
  /hooks
    useUser.ts
    useCalendar.ts
    useStats.ts
    useHours.ts
    usePreferences.ts
    useActivities.ts
  /lib
    api.ts
    slackBot.ts
    dustIntegration.ts
    googleCalendar.ts
    utils.ts
  /assets
    /icons
    /images
  /styles
    tailwind.css
    theme.ts
  App.tsx
  main.tsx
```

---

## 2. Fonctionnalités détaillées par onglet

### 🧩 1. Vue d’ensemble (Dashboard)
- **Résumé hebdomadaire** (WeeklySummaryCard) : jours télétravail, présentiel, congés, total heures, comparatif équipe (anonyme)
- **Planning de la semaine** (Calendar horizontal, avatars collègues)
- **Actions rapides** (QuickActions) : “Je viens aujourd’hui”, “Je télétravaille”, “Je pose un congé”
- **Suggestions sociales** (SocialSuggestions) : “3 collègues seront là mardi…”
- **Mini-feed activités** (ActivityFeed) : projets, activités Slack/Dust
- **Interactions** : hover sur jour → liste collègues, clic sur action → update Slack/Google Calendar

### 📅 2. Calendrier
- **Vue mensuelle/hebdo** (CalendarGrid)
- **Statuts colorés** (présentiel, télétravail, congé, non déclaré)
- **Ajout activité** (CalendarPopup)
- **Double-clic = déclaration rapide**
- **Copier semaine dernière** (WeekCopyButton)
- **Affichage collègues par date** (mini avatars, tooltip)
- **Sync Google Calendar/Lucas**
- **Suggestions automatiques**

### 📊 3. Statistiques
- **Camembert** (PieChart) : répartition télétravail/présentiel/congés
- **Barres empilées** (StackedBarChart) : évolution semaine/semaine
- **Courbe comparée** (TeamComparisonCurve) : vous vs équipe
- **Heatmap** (PresenceHeatmap) : présence par jour de la semaine
- **Filtres** (StatsFilters) : période, lieu, équipe
- **Export** (ExportButtons) : PDF/CSV
- **Résumé mensuel Dust**

### 🕒 4. Horaires
- **Tableau horaires** (HoursTable) : par jour, drag & drop
- **Alertes dépassement** (OvertimeAlert)
- **Créneaux inhabituels**
- **Modification horaires**
- **Règles récurrentes** (RecurringRules)
- **Notifications Slack bienveillantes**

### ⚙️ 5. Préférences
- **Profil utilisateur** (ProfileForm) : nom, rôle, photo, équipe, hobbies
- **Notifications** (NotificationSettings) : Slack/email, fréquence
- **Affichage** (DisplaySettings) : thème, langue, layout
- **Déclaration auto** (basée sur habitudes)
- **Centres d’intérêt** (InterestSelector) : suggestions d’activités

---

## 3. Transversal & Social

- **Encart activités sociales** (SocialSidebar) sur chaque page
  - Prochaines activités, bouton “Je participe”, suggestions selon intérêts
- **Bot Slack intégré** (lib/slackBot.ts)
  - Message matinal “Tu fais quoi aujourd’hui ?”
  - Résumés de présence, projets (via Dust)
- **Animations & UI**
  - Animations douces (shared/AnimatedTransition)
  - Responsive desktop/mobile
  - UI inspirée Notion/Linear/Slack

---

## 4. Cas d’usage clés (à valider)
1. Planifier sa semaine en 2 clics
2. Venir un jour spécifique car des collègues y seront
3. Découvrir une activité spontanée ou un hobby commun
4. Visualiser son rythme de présence sans se comparer
5. Proposer une rencontre en présentiel à un collègue sur le même projet

---

## 5. Stack & intégrations
- **React + TypeScript + Tailwind CSS**
- **Google Workspace API** (calendrier, présence)
- **Slack API** (bot, notifications, feed)
- **Dust** (synthèses projets, suggestions)
- **Lucas** (congés)
- **Backend/API** (Node/Express ou serverless, si besoin)
- **Déploiement** : Vercel, Netlify, ou serveur dédié

---

## 6. Suivi d’avancement (exemple)
- [x] Architecture générale
- [x] Sidebar/navigation dynamique
- [x] Dashboard statique
- [ ] Dashboard dynamique & interactif
- [ ] Calendrier interactif
- [ ] Statistiques graphiques
- [ ] Horaires drag & drop
- [ ] Préférences utilisateur avancées
- [ ] Intégration Slack/Google/Dust
- [ ] Activités sociales transversales
- [ ] Responsive/mobile
- [ ] Animations UI

---

**Tu peux revenir sur cette architecture à tout moment pour :**
- Ajouter des modules
- Prioriser les features
- Suivre ce qui est fait/restant
- Déléguer à une équipe

Prototype fonctionnel incluant au minimum les fonctionnalités essentielles :
    - Interface de déclaration de présence
    - Visualisation des collègues présents/prévus
    - Modification de sa présence
    - Extraction de la liste des présents voila pour les exigences de fonctionnalités 