---
title: Vue d'ensemble du projet
---

<style>
    @media screen and (min-width: 76em) {
        .md-sidebar--primary {
            display: none !important;
        }
    }
</style>

# Vue d'ensemble du projet

!!! info "Informations générales"
    **Session**: Été 2026  
    **Auteur**: Mouhamed Ahmed Tidjani Diop (20290840)<!-- Nom de chaque membre (matricule)  -->  
    **Thèmes**: Génie Logiciel, Développement de plugin, Building Information Modeling<!-- Thèmes principaux abordés dans le projet  -->  
    **Superviseur**: Louis-Edouard Lafontant<!-- Nom du superviseur (affiliation)  -->  
    **Collaborateur:** BPA<!-- Nom de(s) collaborateur(s) et partenaire(s)` -->  

## Description du projet

<!-- > :bulb: N'oubliez pas d'effacer ou mettre en commentaires les notes (`>`) en début de section -->

### Contexte

<!-- > Présentez le contexte général dans lequel s’inscrit votre projet (social, organisationnel, technologique, éducatif, environnemental, etc.). -->

Le secteur de l’architecture, de l’ingénierie et de la construction **(AEC)** utilise de plus en plus les technologies de modélisation des informations du bâtiment **(BIM)** afin de concevoir et gérer des modèles numériques de bâtiments. Parmi les logiciels les plus utilisés dans ce domaine, **Autodesk Revit** permet la conception architecturale et la gestion des données du bâtiment, tandis qu’**Ekahau AI Pro** est utilisé pour la simulation et l’optimisation des réseaux Wi-Fi à l’intérieur des infrastructures.

Ces deux outils sont complémentaires, mais les échanges de données entre **Revit** et **Ekahau** demeurent limités et nécessitent encore plusieurs manipulations manuelles. Cette situation augmente les risques d’erreurs et réduit l’efficacité du flux de travail, particulièrement dans des projets BIM complexes.

Une première version d’un **plugin** Revit–Ekahau a été développée à l’été 2025 afin d’automatiser une partie du processus d’exportation vers **Ekahau**. Le présent projet s’inscrit dans la continuité de ce travail et vise principalement à améliorer la robustesse et la fiabilité des imports et exports d’artéfacts entre les deux logiciels, afin de rendre l’intégration plus stable et mieux adaptée à un contexte professionnel réel.

### Problématique

<!-- > Décrivez le problème central ou la question de recherche que votre projet cherche à adresser, pourquoi s'y intéresser et les faiblesses des solutions actuelles. 
> Le problème doit pouvoir être compris indépendamment de la solution envisagée. -->

Bien que **Revit** et **Ekahau** soient utilisés de manière complémentaire dans les projets de conception et d’analyse des infrastructures réseau, les échanges de données entre ces deux logiciels restent peu fiables et nécessitent encore plusieurs **manipulations manuelles**. Lors de l’exportation ou de l’importation d’artéfacts du modèle BIM, certaines informations peuvent être mal interprétées, incomplètes ou incohérentes entre les deux environnements.

Ces problèmes deviennent particulièrement importants dans des modèles complexes contenant plusieurs niveaux, murs, ouvertures et éléments architecturaux variés. Les erreurs de conversion ou de traitement peuvent alors affecter la qualité des simulations Wi-Fi réalisées dans **Ekahau** et augmenter le temps nécessaire pour corriger manuellement les données.


### Proposition et objectifs
<!-- 
> Présentez votre proposition de projet et les objectifs visés. Expliquez en quoi votre approche répond à la problématique identifiée. 
> Assurez-vous d'avoir, dans la mesure du possible, des objectifs mesurables, raisonnnables dans le temps et non redondants entre eux. -->


Le projet consiste à poursuivre l’amélioration du plugin développé pour faciliter les échanges de données entre **Autodesk Revit** et **Ekahau AI Pro**, en mettant l’accent sur sa robustesse, sa fiabilité et sa maintenabilité dans un contexte d’utilisation réel.

Le travail porte notamment sur la stabilisation des fonctionnalités d’importation et d’exportation existantes, la correction des problèmes observés sur différents modèles BIM ainsi que la prise en charge des environnements ciblés : **Revit 2024 et versions antérieures avec .NET Framework 4.8**, et **Revit 2025 et versions postérieures avec .NET 8.0**.

Une attention particulière sera également portée à l’architecture de la fonctionnalité d’exportation. La première version du plugin étant fortement couplée au format utilisé par **Ekahau**, le projet prévoit une refactorisation visant à mieux séparer l’extraction des données provenant de **Revit** de leur transformation vers un format externe. Cette évolution devra permettre de rendre le code plus modulaire et de réduire la dépendance directe de la logique métier envers **Ekahau**.

Le projet comprend également l’amélioration de l’expérience utilisateur, la préparation de versions facilement installables et testables par **BPA**, ainsi que le nettoyage de la base de code afin de faciliter sa maintenance et son évolution future.

L’objectif final est de disposer d’un plugin plus stable, plus cohérent et plus facilement maintenable pour les échanges entre **Revit** et les flux de planification Wi-Fi réalisés avec **Ekahau AI Pro**.

### Méthodologie

<!-- > Expliquez comment vous comptez aborder le projet : démarche générale, grandes étapes prévues, itérations, types de validations envisagées. -->

Le projet sera réalisé selon une approche **itérative**, en s’appuyant sur la première version du plugin développée à l’été 2025. Les premières étapes consisteront à prendre en main la base de code existante, à comprendre les mécanismes d’importation et d’exportation et à identifier les principales limitations techniques du plugin.

Le développement sera ensuite effectué par cycles successifs de **test, analyse, correction et validation**. Les fonctionnalités seront testées à partir de modèles Revit fournis par **BPA**, ce qui permettra de reproduire des scénarios d’utilisation représentatifs et d’identifier les comportements problématiques sur des projets réels.

Le plugin devant être maintenu pour deux environnements différents, les modifications seront validées sur les versions **.NET 4.8** et **.NET 8.0** lorsque cela sera applicable.

En parallèle des corrections fonctionnelles, une refactorisation progressive de l’architecture sera réalisée afin d’améliorer la séparation des responsabilités et de réduire le couplage entre la logique d’extraction des données Revit et leur transformation vers le format attendu par les outils externes. Cette refactorisation s’appuiera notamment sur le patron de conception **Visitor** et sur l’application de principes de conception tels que le **Single Responsibility Principle (SRP)**.

Enfin, des améliorations UI/UX, du nettoyage de code et des ajustements liés au déploiement seront réalisés progressivement afin d’obtenir une version plus stable et plus facilement maintenable par de futurs développeurs.

### Validation et Évaluation

<!-- > Indiquez comment vous évaluerez que votre solution répond aux objectifs du projet (ex. scénarios d’usage, tests, retours utilisateurs, indicateurs qualitatifs ou quantitatifs). -->


La validation du projet reposera principalement sur des **tests fonctionnels** et des **tests de bout en bout** réalisés sur les différentes versions du plugin.

Les fonctionnalités d’importation et d’exportation seront testées à partir de modèles BIM fournis par **BPA**, comprenant différents niveaux et différentes configurations architecturales. Ces essais permettront de vérifier notamment la cohérence des données exportées, le positionnement des éléments, l’alignement des murs avec les plans générés ainsi que le comportement général du plugin dans des scénarios représentatifs de son utilisation réelle.

Des tests de bout en bout seront également réalisés sur le flux complet :

**Revit → Ekahau → Revit**

Ils permettront de vérifier qu’un modèle peut être exporté depuis Revit, utilisé et modifié dans Ekahau, puis réimporté correctement dans Revit.

La validation sera effectuée sur les deux environnements ciblés :

- **Revit 2024 et versions antérieures** avec **.NET 4.8** ;
- **Revit 2025 et versions postérieures** avec **.NET 8.0**.

La collaboration avec **BPA** permettra enfin de tester le plugin dans son environnement d’utilisation prévu et avec des modèles issus de projets réels.


## Équipe

<!-- > Présentez les membres de l’équipe et le rôle principal de chacun dans le projet. -->

Le projet est réalisé individuellement par **Mouhamed Ahmed Tidjani Diop**, qui est responsable de l’ensemble des activités du projet.


Le projet est principalement encadré par **Louis-Edouard Lafontant** à l’**Université de Montréal**. Il est également réalisé en collaboration avec **BPA**, où **Raymond Alex Lafontant** et **Ramzi Sidani** apportent un encadrement complémentaire lié aux besoins métier, au contexte d’utilisation et à la validation de la solution.

Le support technique lié aux modèles **BIM** et aux usages de Revit est assuré par **Elisabeth Félix**, modélisatrice chez **BPA**.

## Échéancier

!!! info
    Le suivi complet est disponible dans la page [Suivi de projet](suivi.md).

| Activités                                              | Début       | Fin         | Livrable / résultat principal                              | Statut       |
| ------------------------------------------------------ | ----------- | ----------- | ---------------------------------------------------------- | ------------ |
| Définition du projet et analyse préliminaire           | 4 mai       | 17 mai      | Orientation du projet et définition des objectifs          | ✅ Terminé   |
| Formation et mise en place de l’environnement          | 11 mai      | 24 mai      | Environnement de développement Revit fonctionnel           | ✅ Terminé   |
| Analyse du plugin existant et clarification des besoins| 25 mai      | 14 juin     | Analyse technique et identification des améliorations      | ✅ Terminé   |
| Amélioration et validation des fonctionnalités         | 8 juin      | 12 juillet  | Corrections, tests import/export et validation E2E          | ✅ Terminé   |
| Préparation et mise à disposition des versions beta    | 29 juin     | 26 juillet  | Versions .NET Framework 4.8 et .NET 8 disponibles chez BPA | ✅ Terminé   |
| Refactorisation de l’architecture d’exportation        | 6 juillet   | 26 juillet  | Nouvelle architecture basée notamment sur le patron Visitor| ✅ Terminé   |
| Stabilisation des deux versions du plugin              | 13 juillet  | 2 août      | Correction des problèmes d’exportation et d’alignement     | ✅ Terminé   |
| Finalisation du plugin, du rapport et du site de suivi | 3 août | 9 août | Version finale du plugin, rapport finalisé et site de suivi complété | ✅ Terminé |

