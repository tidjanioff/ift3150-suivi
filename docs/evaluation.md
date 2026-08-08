---
title: Évaluation & Discussion
---

<style>
    @media screen and (min-width: 76em) {
        .md-sidebar--primary {
            display: none !important;
        }
    }
</style>


# Évaluation

<!-- > :bulb: Cette page sert à présenter comment le projet a été testé, évalué ou validé.  
> Elle ne remplace pas le rapport final, mais permet de documenter progressivement les résultats obtenus et leur interprétation. -->


Cette section présente les méthodes utilisées pour valider le fonctionnement du plug-in **Revit-Ekahau**, les résultats obtenus au cours des tests ainsi que les principales limites observées.

L’évaluation porte principalement sur la fiabilité des fonctionnalités d’exportation et d’importation entre **Autodesk Revit** et **Ekahau AI Pro**, ainsi que sur leur comportement avec différentes versions de Revit et différents modèles BIM.

## Stratégie de validation

La validation du plug-in a été réalisée principalement à travers des **tests fonctionnels et de bout en bout (E2E)** reproduisant le workflow réel d’utilisation du plug-in.

Les tests ont notamment permis de vérifier :

- l’installation et le chargement du plug-in dans Autodesk Revit ;
- l’exportation des éléments BIM nécessaires vers un projet exploitable dans Ekahau ;
- la conservation des informations associées aux murs, portes et fenêtres ;
- l’importation dans Revit de données modifiées ou ajoutées dans Ekahau ;
- le repositionnement des points d’accès dans le modèle BIM ;
- le fonctionnement du workflow complet **Revit → Ekahau → Revit** ;
- la compatibilité avec différentes versions de Revit et de .NET.

Les tests ont été effectués à la fois sur des modèles utilisés pendant le développement et sur de nouveaux modèles fournis par **BPA**, afin d’éviter de valider le plug-in uniquement sur les projets ayant servi à son implémentation.

## Scénarios testés

### Exportation Revit → Ekahau

Les scénarios d’exportation ont permis de vérifier que les informations nécessaires à la planification Wi-Fi pouvaient être extraites correctement depuis Revit.

Les éléments principalement vérifiés sont :

- les murs ;
- les portes ;
- les fenêtres ;
- leur géométrie ;
- leur position dans le modèle ;
- les propriétés utilisées pour déterminer leur comportement dans Ekahau ;
- les valeurs d’atténuation associées aux différents types d’éléments.

Une attention particulière a également été portée aux modèles contenant des géométries plus complexes ou des configurations susceptibles de mettre en évidence des problèmes dans la logique de traitement des murs.

### Importation Ekahau → Revit

La fonctionnalité d’importation a été validée en réimportant dans Revit les données provenant d’un projet Ekahau.

Les tests ont principalement porté sur :

- la lecture des données provenant du projet Ekahau ;
- le positionnement des points d’accès ;
- la création ou la mise à jour des éléments concernés dans le modèle ;
- la conservation des coordonnées entre les deux environnements.

### Tests de bout en bout

Des tests E2E ont également été réalisés afin de valider le workflow complet :

1. exportation d’un modèle depuis Revit ;
2. ouverture et utilisation du projet dans Ekahau AI Pro ;
3. modification ou ajout de points d’accès ;
4. réimportation des données dans Revit ;
5. vérification du positionnement obtenu dans le modèle BIM.

Cette approche permet de tester non seulement chaque fonctionnalité individuellement, mais également leur interaction dans un scénario représentatif de l’utilisation réelle du plug-in.

## Environnements testés

Deux environnements principaux ont été considérés durant le projet :

| Environnement                        | Plateforme         | État                          |
| ------------------------------------ | ------------------ | ----------------------------- |
| Revit 2024 et versions antérieures   | .NET 4.8 | Workflow export/import validé |
| Revit 2025 et versions plus récentes | .NET 8.0             | Workflow export/import validé |

La version basée sur **.NET Framework 4.8** a fait l’objet de tests complets du workflow d’exportation et d’importation.

La version **.NET 8** a également été testée sur plusieurs modèles Revit, notamment de nouveaux projets fournis par BPA. Les problèmes rencontrés lors des premières phases de validation ont pu être identifiés puis corrigés, permettant de valider le fonctionnement du workflow d’exportation et d’importation sur cette version également.

## Résultats obtenus

Les tests réalisés ont permis de valider les principales fonctionnalités prévues pour le plug-in.

### Fonctionnalités validées

Les éléments suivants ont pu être validés au cours du projet :

- chargement du plug-in dans Autodesk Revit ;
- exportation des informations nécessaires vers Ekahau ;
- traitement des murs, portes et fenêtres ;
- attribution des informations d’atténuation ;
- importation de données provenant d'Ekahau ;
- repositionnement de points d’accès dans Revit ;
- fonctionnement complet du workflow **Revit → Ekahau → Revit** avec Revit 2024 et Revit 2025.

Les tests ont également permis d’identifier plusieurs cas limites qui n’étaient pas apparents lors des premiers essais et d’améliorer progressivement la robustesse du plug-in.

## Analyse des résultats

Les résultats obtenus montrent que le plug-in permet d’automatiser une partie importante des échanges entre les modèles BIM utilisés dans Revit et les projets de planification Wi-Fi réalisés dans Ekahau AI Pro.

Le workflow principal est fonctionnel et peut être exécuté sans avoir à reproduire manuellement dans Ekahau l’ensemble des informations déjà disponibles dans le modèle BIM.

L’un des principaux résultats du projet est également l’amélioration de la maintenabilité de la fonctionnalité d’exportation. La refactorisation réalisée permet de mieux séparer :

- l’extraction des données depuis Revit ;
- la représentation interne de ces données ;
- leur conversion vers un format destiné à un outil externe.

Cette séparation réduit la dépendance directe de la logique d’exportation envers Ekahau et facilite l’évolution future du plug-in.

Les tests réalisés ont cependant montré qu’un fonctionnement correct sur un modèle ne garantit pas nécessairement un comportement identique sur tous les projets Revit. La diversité des géométries, des familles utilisées et de la structure des modèles BIM nécessite donc une validation sur plusieurs projets représentatifs.

## Limites de la validation

### Nombre de modèles testés

Le plug-in a été testé sur plusieurs modèles Revit, notamment des projets fournis par BPA. Il n’a toutefois pas été possible de couvrir l’ensemble des configurations pouvant apparaître dans des projets BIM réels.

Certains comportements dépendent fortement de la manière dont les murs, portes, fenêtres ou autres éléments ont été modélisés.

### Précision géométrique

Sur certains modèles Revit présentant des géométries plus complexes, le traçage généré lors de l’exportation peut présenter de légers écarts par rapport à la géométrie originale du modèle BIM.

Ces écarts n’empêchent pas l’utilisation du résultat dans Ekahau AI Pro, mais la précision du traçage pourrait être améliorée afin de mieux représenter certains cas particuliers, notamment lorsque la géométrie des éléments est plus complexe.

### Accès à Ekahau AI Pro

Ekahau AI Pro étant un logiciel propriétaire nécessitant une licence, l’accès à l’environnement complet de test était principalement possible à travers les ressources mises à disposition par BPA.

Cette contrainte a limité la possibilité d’automatiser certains tests ou de reproduire systématiquement l’ensemble du workflow dans l’environnement de développement.

### Différences entre les versions de Revit

Le passage de **.NET 4.8** à **.NET 8.0** introduit également des différences entre les versions du plug-in.

Même si une grande partie de la logique est commune, certains comportements doivent encore être validés séparément selon la version de Revit utilisée.

### Automatisation des tests

Une partie importante du plug-in dépend directement de l’API Revit et de l’état d’un document BIM ouvert dans Autodesk Revit.

La validation repose donc principalement sur des tests fonctionnels et E2E plutôt que sur une couverture complète par des tests unitaires automatisés.

## Bilan

Dans l’ensemble, les tests réalisés montrent que les fonctionnalités principales de Rekat répondent au besoin identifié au début du projet : faciliter et fiabiliser les échanges entre **Autodesk Revit** et **Ekahau AI Pro**.

Le workflow complet **Revit → Ekahau → Revit** a pu être validé sur les deux environnements ciblés, soit les versions basées sur **.NET 4.8** ainsi que celles basées sur **.NET 8.0**.

Les différentes phases de validation ont également permis d’identifier puis de corriger plusieurs problèmes rencontrés sur certains modèles Revit. Bien que des améliorations restent possibles, notamment concernant la précision du traçage pour certaines géométries complexes, le plug-in atteint les principaux objectifs fonctionnels fixés dans le cadre du projet.

Enfin, les travaux de refactorisation réalisés sur l’architecture du plug-in fournissent une base plus maintenable et extensible pour poursuivre son évolution et intégrer de futures améliorations.