# 📚 ANALYSE_FANTASTIC — Analyse des ventes de livres

## 📌 Présentation du projet

Ce projet de Business Intelligence (BI) consiste à analyser les ventes de livres à l’aide de **SQL Server** et **Power BI**. L’objectif est de transformer les données en indicateurs clés de performance (KPI) et en visualisations interactives afin de faciliter l’analyse des ventes.

## 🎯 Objectifs

* Analyser le volume des ventes par genre de livre.
* Calculer le chiffre d’affaires et le prix moyen unitaire.
* Explorer les ventes selon les dimensions disponibles : temps, département et marketing.
* Concevoir un tableau de bord interactif pour faciliter la prise de décision.
* Mettre en pratique les compétences en SQL, modélisation de données et DAX.

## 🛠️ Technologies utilisées

* **SQL Server** — stockage et gestion des données.
* **Power BI Desktop** — visualisation et création du tableau de bord.
* **DAX** — création des mesures et indicateurs.
* **GitHub** — gestion et partage du projet.

## 🗂️ Modèle de données

Le modèle Power BI s'appuie sur cinq tables :

| Table             | Rôle                                                 |
| ----------------- | ---------------------------------------------------- |
| `Fact_Ventes`     | Table de faits contenant les données de ventes.      |
| `Dim_Livre`       | Informations relatives aux livres et à leurs genres. |
| `Dim_Marketing`   | Dimension relative au marketing et aux magasins.     |
| `Dim_Departement` | Informations relatives aux départements.             |
| `Dim_Temps`       | Dimension temporelle pour l'analyse des périodes.    |

Les tables de dimension sont reliées à la table de faits afin de permettre l'analyse des ventes selon différents axes.

## 📊 Indicateurs clés (KPI)

Le rapport Power BI comprend les mesures DAX suivantes.

### 1. Volume total des ventes

```DAX
Volume Ventes =
SUM(Fact_Ventes[Quantite])
```

Calcule la quantité totale vendue.

### 2. Chiffre d'affaires

```DAX
Chiffre Affaires =
SUMX(
    Fact_Ventes,
    Fact_Ventes[Quantite] * Fact_Ventes[PU]
)
```

Calcule le chiffre d'affaires à partir des quantités vendues et des prix unitaires.

### 3. Prix moyen unitaire

```DAX
Prix Moyen =
AVERAGE(Fact_Ventes[PU])
```

Calcule la moyenne des prix unitaires des lignes de vente.

## 📈 Visualisations Power BI

Le tableau de bord comprend actuellement :

* Des cartes KPI pour le volume des ventes, le chiffre d'affaires et le prix moyen.
* Un graphique du volume des ventes par genre de livre.

Des analyses complémentaires par période, département et marketing pourront enrichir le rapport.

## 🚀 Accès au projet

Le rapport Power BI est disponible dans ce dépôt au format `.pbix`.

Pour consulter et modifier le tableau de bord, téléchargez le fichier puis ouvrez-le avec **Power BI Desktop**.

## 📚 Compétences développées

* Modélisation dimensionnelle.
* Connexion aux données SQL Server.
* Création de mesures avec DAX.
* Conception de tableaux de bord interactifs.
* Analyse des indicateurs de performance commerciale.
* Utilisation de GitHub pour partager un projet BI.

## 🔄 Statut du projet

**En cours de développement.**

Ce projet évoluera avec l'ajout de nouvelles analyses, de visualisations et d'améliorations du tableau de bord.

---

*Projet personnel de mise en pratique des compétences en Business Intelligence et en analyse de données.*
