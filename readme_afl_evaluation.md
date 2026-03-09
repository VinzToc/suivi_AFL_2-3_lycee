# 📊 Application d'Évaluation AFL 2 et 3 - EPS Lycée

## 📝 Description

Application web pour faciliter l'évaluation des **Attendus de Fin de Lycée (AFL)** en Éducation Physique et Sportive, conformément aux programmes officiels français. Cette application permet aux enseignants d'EPS d'évaluer rapidement et efficacement les compétences des élèves sur les AFL 2 et 3, avec un suivi longitudinal des progrès.

## 🎯 Contexte pédagogique

### Les Attendus de Fin de Lycée (AFL) en EPS

Dans le cadre de la réforme du lycée, l'évaluation en EPS s'appuie sur **5 Attendus de Fin de Lycée (AFL)**. Cette application se concentre sur deux d'entre eux :

#### **AFL 2 : S'entraîner pour améliorer ses performances**
Cet attendu évalue la capacité de l'élève à :
- **Se préparer** : Planifier et organiser son entraînement
- **S'entraîner** : Mettre en œuvre des stratégies d'amélioration de ses performances

#### **AFL 3 : Exercer des rôles sociaux**
Cet attendu évalue la capacité de l'élève à :
- **Échauffement** : Préparer son corps à l'effort de manière autonome et adaptée
- **Observateur** : Analyser et évaluer la performance d'un pair
- **Coach** : Conseiller et accompagner un camarade dans sa progression

### Système d'évaluation par niveaux

Chaque compétence est évaluée sur **4 niveaux** :
- **Niveau 1** : Maîtrise insuffisante
- **Niveau 2** : Maîtrise fragile
- **Niveau 3** : Maîtrise satisfaisante
- **Niveau 4** : Très bonne maîtrise

### Répartition des points

L'élève choisit la répartition des points entre AFL 2 et AFL 3 selon ses points forts :
- **6 pts AFL2 / 2 pts AFL3** : L'élève privilégie l'entraînement personnel
- **4 pts AFL2 / 4 pts AFL3** : Répartition équilibrée
- **2 pts AFL2 / 6 pts AFL3** : L'élève privilégie les rôles sociaux

## ✨ Fonctionnalités

### 📋 Gestion des élèves
- **Import CSV** : Importation d'une liste d'élèves depuis un fichier CSV (colonne A)
- **Liste déroulante** : Sélection rapide de l'élève à évaluer
- **Informations contextuelles** : Classe et date de séance

### 📊 Évaluation interactive
- **Curseurs gradués** : Évaluation visuelle sur 4 niveaux pour chaque compétence
- **Noms d'items personnalisables** : Adaptation des intitulés selon l'activité (gymnastique, natation, badminton, etc.)
- **Choix de répartition** : Curseur pour sélectionner la pondération AFL2/AFL3

### 💾 Suivi longitudinal
- **Import Excel** : Récupération d'un fichier d'évaluation existant
- **Historique** : Visualisation de toutes les évaluations précédentes de l'élève
- **Export cumulatif** : Ajout automatique de la nouvelle évaluation aux données existantes

### 📤 Export des données
- **Format Excel (.xlsx)** : Compatible avec tous les tableurs
- **Nomenclature standardisée** : `AFL_Evaluation-NOM_PRENOM-CLASSE.xlsx`
- **Structure organisée** : En-têtes de colonnes + données d'évaluation
- **Date au format français** : JJ/MM/AA

## 🚀 Installation et utilisation

### Prérequis
- Navigateur web moderne (Chrome, Firefox, Safari, Edge)
- Aucune connexion internet requise après téléchargement
- Compatible PC et tablettes (modes portrait et paysage)

### Installation
1. Téléchargez le fichier HTML de l'application
2. Ouvrez-le avec votre navigateur web
3. L'application fonctionne entièrement en local

### Workflow type

#### 🆕 Première évaluation d'une classe

1. **Préparation** : Créez un fichier CSV avec la liste de vos élèves (nom et prénom en colonne A)
2. **Import** : Cliquez sur "📋 Importer CSV" et sélectionnez votre fichier
3. **Évaluation** :
   - Sélectionnez un élève dans la liste déroulante
   - Renseignez la classe et la date
   - Personnalisez les noms des items selon l'activité pratiquée
   - L'élève choisit sa répartition de points
   - Évaluez chaque compétence avec les curseurs (1 à 4)
4. **Export** : Cliquez sur "📊 Exporter en Excel"
5. **Répétez** pour chaque élève

#### 🔄 Évaluations suivantes (suivi longitudinal)

1. **Import** : Cliquez sur "📊 Importer Excel" et sélectionnez le fichier de l'élève
2. **Historique** : Consultez les évaluations précédentes affichées automatiquement
3. **Nouvelle évaluation** : Renseignez la date du jour et évaluez les nouvelles compétences
4. **Export** : Le fichier Excel contiendra toutes les évaluations (anciennes + nouvelle)

## 📁 Structure des fichiers

### Fichier CSV d'import (liste d'élèves)
```csv
DUPONT Jean
MARTIN Sophie
BERNARD Lucas
PETIT Emma
```

### Fichier Excel généré
**Nom** : `AFL_Evaluation-DUPONT_Jean-2nde3.xlsx`

**Contenu** :
| Date | Répartition Points | AFL2 Item 1 | AFL2 Item 2 | AFL3 Item 1 | AFL3 Item 2 | AFL3 Item 3 |
|------|-------------------|-------------|-------------|-------------|-------------|-------------|
| 15/01/26 | AFL2 = 4pts / AFL3 = 4pts | 2 | 3 | 2 | 3 | 3 |
| 29/01/26 | AFL2 = 4pts / AFL3 = 4pts | 3 | 3 | 3 | 3 | 4 |

## 🎨 Interface utilisateur

### En-tête
- Titre de l'application
- Boutons d'import (CSV et Excel)

### Zone d'information élève
- Bandeau bleu affichant nom et classe (mode import Excel)
- Historique des évaluations en jaune (mode import Excel)
- Champs élève/classe/date (mode normal)

### Zone de répartition des points
- Curseur à 3 positions
- Affichage dynamique du choix

### Zones d'évaluation
- **AFL 2** : 2 items personnalisables avec curseurs gradués
- **AFL 3** : 3 items personnalisables avec curseurs gradués
- Graduations visuelles (1, 2, 3, 4)
- Affichage du niveau sélectionné

### Bouton d'export
- Bouton violet en bas de page
- Export instantané au format Excel

## 💻 Technologies utilisées

- **HTML5** : Structure de l'application
- **CSS3** : Design moderne et responsive
- **JavaScript** : Logique applicative
- **PapaParse** : Lecture des fichiers CSV
- **SheetJS (XLSX)** : Lecture et écriture des fichiers Excel

## 🔧 Personnalisation

### Adapter les items d'évaluation
Les noms des items peuvent être personnalisés selon l'activité :

**Exemple Badminton** :
- AFL2 Item 1 : "Gérer son échauffement spécifique"
- AFL2 Item 2 : "S'entraîner aux frappes hautes"
- AFL3 Item 1 : "Échauffement articulaire poignets/épaules"
- AFL3 Item 2 : "Observer et scorer un match"
- AFL3 Item 3 : "Conseiller sur le placement terrain"

**Exemple Natation** :
- AFL2 Item 1 : "Planifier ses séries d'entraînement"
- AFL2 Item 2 : "Améliorer sa technique de virage"
- AFL3 Item 1 : "Échauffement à sec et étirements"
- AFL3 Item 2 : "Chronométrer et analyser les temps"
- AFL3 Item 3 : "Coacher sur la respiration"

## 📱 Compatibilité

- ✅ PC (Windows, Mac, Linux)
- ✅ Tablettes iPad et Android
- ✅ Mode portrait et paysage
- ✅ Fonctionnement hors ligne
- ✅ Pas d'installation requise

## 🤝 Contribution

Cette application est conçue pour être facilement adaptable aux besoins spécifiques de chaque enseignant. N'hésitez pas à proposer des améliorations ou des nouvelles fonctionnalités.

## 📄 Licence

Application développée pour l'Éducation Nationale française. Libre d'utilisation pour les enseignants d'EPS.

## 👨‍🏫 Support

Pour toute question ou suggestion d'amélioration, n'hésitez pas à ouvrir une issue sur ce repository.

---

**Développé avec ❤️ pour faciliter l'évaluation en EPS** 🏃‍♂️🏊‍♀️🤸‍♂️