# Site de suivi — Projet IFT3150
 
Ce dépôt contient le **site de suivi du projet réalisé dans le cadre du cours IFT3150 – Projet informatique** à l'Université de Montréal.
 
Le projet porte sur l'amélioration d'un **plug-in Autodesk Revit** destiné à faciliter et fiabiliser les échanges de données entre des modèles BIM dans **Autodesk Revit** et des projets de planification Wi-Fi dans **Ekahau AI Pro**.
 
Le site est construit avec [MkDocs](https://www.mkdocs.org/) et le thème [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).
 
## Contenu du site
 
Le site regroupe notamment :
 
- la présentation et le contexte du projet ;
- les objectifs et besoins identifiés ;
- le suivi hebdomadaire du travail réalisé ;
- la conception et la réalisation technique ;
- les principales difficultés rencontrées et décisions prises ;
- les tests et la validation du plug-in ;
- les résultats et le bilan du projet.
## Technologies
 
Le site de suivi utilise principalement :
 
- **MkDocs**
- **Material for MkDocs**
- **Markdown**
- **GitHub Pages**
Le projet documenté repose notamment sur :
 
- **C# / .NET**
- **Autodesk Revit API**
- **WPF / XAML**
- **Ekahau AI Pro**
## Utilisation locale
 
### Prérequis
 
- Python **3.11** ou plus récent
- `pip`
### Installation
 
Installez les dépendances :
 
```bash
pip install -r requirements.txt
```
 
Lancez ensuite le serveur MkDocs local :
 
```bash
mkdocs serve --livereload
```
 
Le site sera accessible à l'adresse :
 
```
http://127.0.0.1:8000
```
 
## Déploiement
 
Pour générer la version statique du site :
 
```bash
mkdocs build
```
 
Pour déployer ou mettre à jour le site sur GitHub Pages :
 
```bash
mkdocs gh-deploy
```
 
## Structure du dépôt
 
```
.
├── docs/
│   ├── index.md
│   ├── suivi.md
│   ├── realisation.md
│   ├── validation.md
│   └── ...
├── mkdocs.yml
├── requirements.txt
└── README.md
```
 
Le contenu principal du site se trouve dans le dossier `docs/`.
 
## Contexte académique
 
Projet réalisé durant la session d'été 2026 dans le cadre du cours IFT3150 – Projet informatique du Département d'informatique et de recherche opérationnelle (DIRO) de l'Université de Montréal, en collaboration avec **BPA** et sous la supervision de **Louis-Edouard Lafontant**.