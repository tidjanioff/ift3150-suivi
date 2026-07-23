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
        - Présentation des outils et méthodes de travail utilisés dans l’entreprise dans le cadre du projet
        - Identification des ressources disponibles pour le projet


## Semaine 6 (8–14 juin)

### Objectifs de la période
- Commencer à travailler dans les locaux de BPA une fois par semaine
- Évaluer l’état actuel du plugin
- Identifier les améliorations prioritaires à apporter

### Travail réalisé

!!! abstract "Avancement"
    - [x] Travail effectué dans les locaux de BPA sous la supervision de **Raymond Alex Lafontant** et **Ramzi Sidani**
    - [x] Prise en main du logiciel **Ekahau** dans l’environnement de BPA
        - Accès à une licence complète du logiciel disponible sur les postes de travail de l’entreprise
        - Exploration de l’interface et des fonctionnalités pertinentes au projet
        - Familiarisation avec la structure des projets et des données utilisées par le plugin
    - [x] Audit de la version actuelle du plugin
        - Analyse du fonctionnement général de la fonctionnalité d’exportation
        - Évaluation de l’expérience utilisateur offerte par l’interface actuelle
        - Identification des principaux points d’amélioration UI/UX
    - [x] Début de la refonte de certains éléments de l’interface utilisateur
    - [x] Début des travaux de correction de bogues
        - Analyse des problèmes affectant la compatibilité avec les versions antérieures de Revit
        - Intervention sur la version **.NET Framework 4.8** utilisée pour **Revit 2024 et versions antérieures**
        - Identification de plusieurs comportements instables nécessitant des correctifs

## Semaine 7 (15–21 juin)

### Objectifs de la période

* Tester la fonctionnalité d’exportation dans différents scénarios
* Vérifier le bon fonctionnement du plugin sur les deux environnements ciblés
* Corriger les bogues bloquant ou affectant l’export

### Travail réalisé

!!! abstract "Avancement"
    - [x] Réalisation de tests sur la fonctionnalité d’exportation du plugin
        - Tests effectués sur différents scénarios d’utilisation
        - Vérification du comportement de l’export selon la structure des plans Revit
    - [x] Validation de l’export sur les deux versions du plugin
        - Version compatible **Revit 2025** avec **.NET 8**
        - Version compatible **Revit 2024 et versions antérieures** avec **.NET Framework 4.8**
    - [x] Correction de bogues liés au processus d’exportation
    - [x] Préparation des prochains tests
        - Identification du besoin de plans Revit plus complexes pour mieux valider le comportement du plugin
        - Demande faite à **Ramzi Sidani** afin d’obtenir des plans réels de BPA pour les prochaines phases de test

### Difficultés rencontrées

!!! warning "Difficultés"
    - Les tests sur **Revit 2024** ont été limités par le manque de plans disponibles
        - Un seul plan était disponible pour cette version
        - Ce plan ne contenait qu’un seul niveau, ce qui n’a pas permis de tester l’exportation dans un scénario multi-niveaux
    - Des plans plus complexes ont été demandés à BPA afin de poursuivre les tests de manière plus représentative la semaine suivante

## Semaine 8 (22–28 juin)

### Objectifs de la période

* Poursuivre les tests de validation du plugin avec des plans réels fournis par BPA
* Mettre l'accent sur les tests de la fonctionnalité d'import

### Travail réalisé

!!! abstract "Avancement"
    - [x] Réalisation de tests sur la fonctionnalité d’importation du plugin
        - Tests effectués à partir des données Ekahau et des plans Revit disponibles
        - Vérification du comportement de l’importation des points d’accès dans Revit
        - Observation des interactions entre les données importées et les éléments du modèle Revit
    - [x] Finalisation des tests d’exportation avec **Revit 2024**
        - Utilisation de plans réels fournis par **BPA**
        - Validation du comportement de l’exportation avec la version **.NET Framework 4.8**
    - [x] Finalisation de la pile de tests **Import/Export** pour la version compatible **Revit 2024 et versions antérieures**
        - Tests réalisés sur la version du plugin basée sur **.NET Framework 4.8**
        - Validation du fonctionnement général selon les scénarios disponibles
    - [x] Préparation des tests pour la version compatible **Revit 2025**
        - Analyse du projet Revit 2025 fourni par BPA
        - Identification d’un blocage empêchant la validation complète avec **.NET 8**

### Difficultés rencontrées

!!! warning "Difficultés"
    - Les tests sur la version compatible **Revit 2025** avec **.NET 8** n’ont pas pu être complétés
    - Le projet Revit 2025 fourni ne contenait aucun **floor plan**
    - L’absence de plans exploitables empêchait de tester correctement les fonctionnalités d’importation et d’exportation
    - La validation complète de la version **.NET 8** a donc été reportée à la semaine suivante

## Semaine 9 (29 juin – 05 juillet)

### Objectifs de la période

* Terminer les tests d'import/export pour la version **.NET 8** avec les plans fournis par BPA
* Déployer localement une première version beta du plugin

### Travail réalisé

!!! abstract "Avancement"
    - [x] Réalisation d’un premier déploiement local du plugin pour la version **.NET Framework 4.8**
        - Déploiement effectué pour la version compatible **Revit 2024 et versions antérieures**
        - Validation basée sur les tests d’importation et d’exportation réalisés avec les plans fournis par **BPA**
    - [x] Poursuite des tests sur la version compatible **Revit 2025** avec **.NET 8**
        - Analyse d’un projet Revit de **BPA** lié à un contexte d’aéroport
        - Identification de problèmes empêchant un déploiement fiable de cette version
    - [x] Début de l’investigation des problèmes spécifiques à la version **.NET 8**
        - Analyse des comportements problématiques observés avec le projet fourni
        - Report du déploiement de la version **Revit 2025 / .NET 8** jusqu’à correction des problèmes identifiés

### Difficultés rencontrées

!!! warning "Difficultés"
    - Le déploiement local n’a pu être réalisé que pour la version **.NET Framework 4.8**
    - Les tests effectués avec les plans fournis par **BPA** étaient concluants pour cette version
    - La version **.NET 8** compatible **Revit 2025** présente encore des problèmes avec un projet réel de BPA
    - Les difficultés observées empêchent un déploiement local fiable pour le moment
    - Une analyse plus approfondie est nécessaire afin d’identifier précisément les causes et d’appliquer les correctifs requis


## Semaine 10 (6–12 juillet)

### Objectifs de la période

* Valider l’ensemble du flux d’utilisation du plugin sur Revit 2024
* Préparer une version facilement installable et testable par les utilisateurs
* Poursuivre l’analyse des problèmes rencontrés avec Revit 2025
* Préparer une refactorisation majeure de la fonctionnalité d’exportation

### Travail réalisé

!!! abstract "Avancement"
    - [x] Réalisation de tests de bout en bout sur la version compatible Revit 2024 et versions antérieures
        - Validation du flux complet Revit → Ekahau → Revit
        - Exportation d’un projet Revit vers Ekahau
        - Modification du projet dans Ekahau, notamment par le placement de points d’accès
        - Réimportation des données Ekahau dans Revit
        - Confirmation du bon fonctionnement général des fonctionnalités d’importation et d’exportation avec .NET Framework 4.8
    - [x] Préparation d’un dossier d’installation téléchargeable pour la version Revit 2024
        - Regroupement des fichiers nécessaires au fonctionnement du plugin
        - Organisation des ressources et des fichiers de configuration requis
    - [x] Poursuite de l’analyse des problèmes rencontrés avec Revit 2025 / .NET 8
        - Constat que les problèmes observés ne semblent pas directement liés à une incompatibilité technique évidente avec Revit 2025
        - Identification du projet d’aéroport YUL utilisé pour les tests comme cause potentielle des comportements problématiques
        - Demande d’un autre projet Revit 2025 à BPA afin de déterminer si le problème provient du plugin ou des particularités du modèle testé
    - [x] Début de la conception d’une refactorisation majeure de la fonctionnalité d’exportation
        - Analyse des dépendances actuelles entre le plugin et le format de projet Ekahau
        - Définition sur papier d’une nouvelle architecture avant modification de la base de code
        - Objectif de rendre le processus d’exportation indépendant d’Ekahau
        - Préparation d’une séparation plus claire entre l’extraction des données Revit et leur transformation vers un format exploitable par des outils externes

### Difficultés rencontrées

!!! warning "Difficultés"
    - La validation de la version compatible Revit 2025 / .NET 8 demeure incomplète
    - Les problèmes observés apparaissent principalement avec le projet d’aéroport YUL fourni par BPA
    - L’origine exacte du problème n’a pas encore pu être déterminée
    - Des tests avec un autre projet Revit 2025 sont nécessaires afin d’isoler la source du problème

## Semaine 11 (13–19 juillet)

### Objectifs de la période

* Finaliser la conception de la nouvelle architecture de la fonctionnalité d’exportation
* Commencer l’implémentation de la refactorisation
* Tester la version Revit 2025 / .NET 8 avec de nouveaux plans fournis par BPA
* Déterminer si les problèmes observés proviennent des modèles testés ou du plugin

### Travail réalisé

!!! abstract "Avancement"
    - [x] Finalisation de la conception de la nouvelle architecture de la fonctionnalité d’exportation
        - Précision des responsabilités des différentes composantes
        - Définition d’une séparation plus claire entre l’extraction des données Revit et leur transformation vers des formats externes
        - Préparation d’une architecture visant à réduire la dépendance directe envers Ekahau
    - [x] Début de l’implémentation de la nouvelle architecture
        - Création des premières composantes issues de la conception
        - Début de l’adaptation du code existant à la nouvelle structure
        - Progression graduelle afin de préserver le fonctionnement actuel pendant la refactorisation
    - [x] Réalisation de tests avec de nouveaux plans Revit 2025 fournis par BPA
        - Vérification du comportement de la version basée sur **.NET 8**
        - Reproduction de problèmes similaires à ceux observés avec le projet d’aéroport YUL
        - Confirmation que les difficultés ne sont pas propres à un seul modèle Revit

### Difficultés rencontrées

!!! warning "Difficultés"
    - Des problèmes persistent avec la version compatible **Revit 2025 / .NET 8**, malgré l’utilisation de nouveaux plans
    - Les nouveaux tests indiquent que la source du problème se situe vraisemblablement dans le plugin plutôt que dans les particularités des modèles fournis
    - Une investigation plus approfondie du processus d’exportation est nécessaire
    - Les prochaines étapes consisteront à isoler les causes des comportements observés et à corriger les bogues afin de stabiliser cette version

<!-- ## Semaine X (y-z mois)

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
        - Résolu après nettoyage et configuration correcte dans `mkdocs.yml` -->
