---
title: Suivi du projet
---

<style>
    @media screen and (min-width: 76em) {
        .md-sidebar--primary {
            display: none !important;
        }
    }
</style>

# Suivi de projet

> :bulb: Cette page documente l’évolution du projet dans le temps.
> Elle sert à rendre visibles les décisions, ajustements et apprentissages.
> Les entrées peuvent être hebdomadaires ou bi-hebdomadaires.  
> N'oubliez pas d’effacer ou de mettre en commentaires les notes (`>`) avant la remise finale.

---

## Semaine 1 (4–10 mai)

### Objectifs de la période
- Définir l’orientation du projet 
- Explorer les différents axes possibles du projet
- Identifier une solution pertinente et réalisable

### Travail réalisé

!!! abstract "Avancement"
    - [x] Confirmation du choix du projet de plugin Revit avec BPA
    - [x] Discussion et analyse de plusieurs axes de projet possibles
        - Axe 1 : amélioration de la robustesse et de la fiabilité des imports/exports d’artéfacts entre Revit et Ekahau
        - Axe 2 : amélioration de la détection des murs via des techniques d’analyse d’image
        - Axe 3 : conception d’une version légère web de Revit permettant un aperçu rapide des projets
    - [x] Analyse de la faisabilité et de la portée des différentes approches
    - [x] Sélection de l’axe principal du projet
        - Choix de l’axe 1 pour la suite du développement


## Semaine 2 (11–17 mai)

### Objectifs de la période
- Monter en compétence sur les technologies requises pour le projet
- Préparer un environnement de développement fonctionnel
- Commencer l’exploration du développement Revit

### Travail réalisé

!!! abstract "Avancement"
    - [x] Apprentissage des bases de **C#** et du framework **.NET**
        - Suivi de cours et exercices pratiques (Code with Mosh)
    - [x] Début d’exploration du développement desktop avec **WPF**
        - Tutoriel Microsoft : *Tutorial: Create a WPF app with .NET*
    - [x] Exploration initiale du développement de plugins Revit
        - Lecture du tutoriel Autodesk : *My First Revit Plug-in Overview*
    - [x] Identification des contraintes techniques liées à l’environnement de développement
        - Incompatibilité initiale avec macOS (absence de support Revit / limitations pour le développement WPF)
    - [x] Mise en place d’une solution alternative
        - Réception d’un poste Windows fourni par le superviseur

### Difficultés rencontrées

!!! warning "Difficultés"
    - L’environnement de développement n’a pas pu être pleinement configuré cette semaine
        - Revit n’étant pas disponible sur macOS, le développement natif du plugin était bloqué
        - Le poste Windows fourni utilise un compte standard sans privilèges administrateur
        - Impossible d’installer Visual Studio, ce qui a empêché la réalisation complète des tutoriels et la pratique concrète
    - Résolution prévue en début de semaine suivante après ajustement des accès

## Semaine 3 (18-24 mai)

### Objectifs de la période
- Finaliser la configuration de l’environnement de développement
- Développer une première expérience pratique avec l’API Revit

### Travail réalisé

!!! abstract "Avancement"
    - [x] Résolution des problèmes de configuration de l’environnement de développement
        - Obtention des accès nécessaires sur le poste Windows
        - Installation et configuration des outils requis (i.e. **Visual Studio**)
    - [x] Mise en place d’un environnement de développement pleinement fonctionnel pour le développement de plugin Revit
    - [x] Réalisation du tutoriel Autodesk : *My First Revit Plug-in*
        - Création d’un premier plugin fonctionnel en **C#**
        - Compréhension de la structure d’un plugin Revit (**IExternalCommand**, transactions, interaction avec le document actif)
        - Compilation, déploiement et exécution du plugin dans Revit



## Semaine 4 (25–31 mai)

### Objectifs de la période
- Se familiariser avec le code existant du plugin
- Comprendre l’architecture de la première itération du projet
- Analyser le fonctionnement du processus d’importation entre Ekahau et Revit

### Travail réalisé

!!! abstract "Avancement"
    - [x] Prise en main de la base de code développée lors de la première itération du projet
    - [x] Étude approfondie du mécanisme d’importation des données
        - Analyse des classes responsables de l’importation
        - Compréhension du rôle et du fonctionnement du fichier **Import.cs**
        - Exploration des interactions entre les données Ekahau et les éléments créés dans Revit
    - [x] Identification des principales composantes impliquées dans le processus d’import


## Semaine 5 (1–7 juin)

### Objectifs de la période
- Clarifier les attentes du partenaire industriel
- Mieux comprendre le contexte d’utilisation du plugin
- Définir un plan de travail pour les prochaines semaines

### Travail réalisé

!!! abstract "Avancement"
    - [x] Rencontre avec l’équipe de BPA
        - Présentation plus détaillée du contexte du projet
        - Discussion sur les objectifs et les priorités de développement
        - Clarification des attentes concernant l’amélioration du plugin
    - [x] Définition d’un plan de travail préliminaire pour les prochaines phases du projet
    - [x] Découverte de l’environnement de travail de BPA
        - Visite des locaux
        - Présentation des outils et méthodes de travail utilisés dans l’entreprise
        - Identification des ressources disponibles pour le projet

## Semaine X (y-z mois)

### Objectifs de la période
- Clarifier la problématique
- Explorer les solutions existantes
- Produire un premier prototype conceptuel

### Travail réalisé

!!! abstract "Avancement"
    - [x] Analyse de solutions existantes
        - Comparaison de trois outils similaires
    - [x] Prototype basse fidélité (Figma)
    - [ ] Validation utilisateur
        - Reportée à la semaine suivante

### Décisions et ajustements

> À compléter uniquement si des choix structurants ont été faits
> ou si l’orientation du projet a évolué.

!!! info "Décisions"
    - Abandon de l’approche X jugée trop complexe
    - Reformulation de la problématique suite aux premières analyses

### Difficultés rencontrées

> À compléter uniquement si des obstacles ont eu un impact réel
> sur l’avancement du projet.

!!! warning "Difficultés"
    - Problème de configuration du plugin Mermaid
        - Confusion entre `mkdocs-mermaid2-plugin` (pip)
          et `mermaid2` (nom du plugin)
        - Résolu après nettoyage et configuration correcte dans `mkdocs.yml`
