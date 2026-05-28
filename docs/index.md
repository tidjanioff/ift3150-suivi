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

> :bulb: N'oubliez pas d'effacer ou mettre en commentaires les notes (`>`) en début de section

### Contexte

> Présentez le contexte général dans lequel s’inscrit votre projet (social, organisationnel, technologique, éducatif, environnemental, etc.).

Le secteur de l’architecture, de l’ingénierie et de la construction **(AEC)** utilise de plus en plus les technologies de modélisation des informations du bâtiment **(BIM)** afin de concevoir et gérer des modèles numériques de bâtiments. Parmi les logiciels les plus utilisés dans ce domaine, **Autodesk Revit** permet la conception architecturale et la gestion des données du bâtiment, tandis qu’**Ekahau** est utilisé pour la simulation et l’optimisation des réseaux Wi-Fi à l’intérieur des infrastructures.

Ces deux outils sont complémentaires, mais les échanges de données entre **Revit** et **Ekahau** demeurent limités et nécessitent encore plusieurs manipulations manuelles. Cette situation augmente les risques d’erreurs et réduit l’efficacité du flux de travail, particulièrement dans des projets BIM complexes.

Une première version d’un **plugin** Revit–Ekahau a été développée à l’été 2025 afin d’automatiser une partie du processus d’exportation vers Ekahau. Le présent projet s’inscrit dans la continuité de ce travail et vise principalement à améliorer la robustesse et la fiabilité des imports et exports d’artéfacts entre les deux logiciels, afin de rendre l’intégration plus stable et mieux adaptée à un contexte professionnel réel.

### Problématique

> Décrivez le problème central ou la question de recherche que votre projet cherche à adresser, pourquoi s'y intéresser et les faiblesses des solutions actuelles. 
> Le problème doit pouvoir être compris indépendamment de la solution envisagée.

Bien que Revit et Ekahau soient utilisés de manière complémentaire dans les projets de conception et d’analyse des infrastructures réseau, les échanges de données entre ces deux logiciels restent peu fiables et nécessitent encore plusieurs manipulations manuelles. Lors de l’exportation ou de l’importation d’artéfacts du modèle BIM, certaines informations peuvent être mal interprétées, incomplètes ou incohérentes entre les deux environnements.

Ces problèmes deviennent particulièrement importants dans des modèles complexes contenant plusieurs niveaux, murs, ouvertures et éléments architecturaux variés. Les erreurs de conversion ou de traitement peuvent alors affecter la qualité des simulations Wi-Fi réalisées dans Ekahau et augmenter le temps nécessaire pour corriger manuellement les données.

La première version du plugin développée en 2025 a permis d’automatiser une partie des échanges entre Revit et Ekahau, notamment dans l'exportation des éléments de Revit vers Ekahau, mais plusieurs limitations liées à la robustesse et à la fiabilité du traitement des données demeurent présentes. Il devient donc nécessaire d’améliorer la stabilité des imports et exports afin de réduire les erreurs, assurer une meilleure cohérence des données et rendre l’intégration plus adaptée à une utilisation professionnelle réelle.

### Proposition et objectifs

> Présentez votre proposition de projet et les objectifs visés. Expliquez en quoi votre approche répond à la problématique identifiée. 
> Assurez-vous d'avoir, dans la mesure du possible, des objectifs mesurables, raisonnnables dans le temps et non redondants entre eux.

Le projet consiste à améliorer le plugin développé pour l’intégration entre Revit et Ekahau, en mettant principalement l’accent sur la robustesse et la fiabilité des échanges de données entre les deux logiciels. Bien que la partie exportation de Revit vers Ekahau soit déjà largement fonctionnelle, plusieurs défis demeurent présents, notamment en raison de l’absence d’API officielle fournie par Ekahau.

Cette absence d’API oblige le plugin à générer directement les fichiers internes utilisés par Ekahau, ce qui crée des risques d’incompatibilité lorsque la structure interne du logiciel évolue selon les versions. Le projet vise donc à mettre en place des mécanismes de vérification et de validation de la structure des fichiers Ekahau avant la génération des données, afin d’améliorer la compatibilité et la stabilité du plugin.

Le projet mettra également davantage l’accent sur la fonctionnalité d’importation depuis Ekahau vers Revit, qui demeure moins avancée que la partie exportation. L’objectif est d’assurer une importation plus fiable et plus cohérente des artéfacts et des informations provenant des simulations réalisées dans Ekahau.

L’objectif final est de rendre l’intégration entre Revit et Ekahau plus stable, plus fiable et mieux adaptée à une utilisation professionnelle réelle.

### Méthodologie

> Expliquez comment vous comptez aborder le projet : démarche générale, grandes étapes prévues, itérations, types de validations envisagées.

Le projet sera réalisé de manière itérative en s’appuyant sur la première version du plugin développée à l’été 2025. Une première étape consistera à analyser l’architecture existante ainsi que les mécanismes actuels d’importation et d’exportation entre Revit et Ekahau afin d’identifier les principales sources d’erreurs et d’incompatibilités.

Par la suite, une étude de la structure interne des fichiers Ekahau sera effectuée pour vérifier les variations possibles selon les versions du logiciel. Cette étape permettra de mettre en place des mécanismes de validation avant la génération ou l’importation des données afin de réduire les risques d’incompatibilité.

Le développement portera principalement sur l’amélioration de la robustesse du traitement des données ainsi que sur la fonctionnalité d’importation depuis Ekahau vers Revit. Les différentes fonctionnalités seront développées progressivement et intégrées au plugin existant afin de valider leur comportement dans des scénarios réels d’utilisation.

### Validation et Évaluation

> Indiquez comment vous évaluerez que votre solution répond aux objectifs du projet (ex. scénarios d’usage, tests, retours utilisateurs, indicateurs qualitatifs ou quantitatifs).

L’évaluation du projet reposera principalement sur la stabilité et la fiabilité des échanges de données entre Revit et Ekahau. Des tests seront réalisés afin de vérifier que les fichiers générés ou importés demeurent compatibles avec différentes structures de projets Ekahau et différentes versions du logiciel.

Des tests unitaires et des tests d’intégration seront également effectués sur les principales fonctionnalités du plugin, particulièrement celles liées à l’importation des données depuis Ekahau vers Revit. Ces tests permettront de vérifier la cohérence des données importées, le bon positionnement des artéfacts dans le modèle BIM ainsi que la réduction des erreurs de traitement.

Finalement, des validations seront réalisées sur des modèles BIM de différentes tailles et complexités afin d’évaluer le comportement du plugin dans des scénarios d’utilisation plus proches d’un contexte professionnel réel.


## Équipe

> Présentez les membres de l’équipe et le rôle principal de chacun dans le projet.

Le projet est réalisé individuellement par **Mouhamed Ahmed Tidjani Diop**.

<!-- ### Rôle principal
- ...
- ... -->

Le projet est encadré par **Louis-Edouard Lafontant** et réalisé en collaboration avec **BPA**, qui agit comme partenaire externe pour la définition du besoin et la validation de la solution.

## Échéancier

!!! info
    Le suivi complet est disponible dans la page [Suivi de projet](suivi.md).

| Activités                      | Début   |   Fin   | Livrable                            | Statut      |
|--------------------------------|---------|---------|-------------------------------------|-------------|
| Ouverture de projet            | 4 mai   | 15 mai  | Proposition de projet               | ✅ Terminé  |
| Études préliminaires           | 4 mai   | 22 mai  | Document d'analyse                  | 🔄 En cours |
| Présentation + Rapport         | 7 aout  | 14 aout | Présentation + Rapport              | ⏳ À venir  |
