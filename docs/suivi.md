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
- Définir l’orientation du projet avec BPA
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
- Se familiariser avec les technologies du projet
- Comprendre le développement de plugins Revit
- Préparer l’environnement de développement

### Travail réalisé

!!! abstract "Avancement"
    - [x] Installation et configuration de l’environnement de développement
    - [x] Prise en main du langage C# et du framework .NET
    <!-- - [x] Exploration de la documentation liée à l’API Revit -->
    - [x] Réalisation du tutoriel Autodesk
        - *My First Revit Plug-in Overview*
    - [x] Compréhension de la structure et du fonctionnement de base d’un plugin Revit


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
