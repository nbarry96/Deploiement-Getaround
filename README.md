# Projet de Déploiement GetAround - Analyse des Retards et Prédiction des Prix de Location de Voiture
## I. Inroduction
GetAround est l'Airbnb des voitures. Vous pouvez louer des voitures à n’importe qui pour quelques heures à quelques jours ! Fondée en 2009, cette entreprise a connu une croissance rapide. En 2019, ils comptent plus de 5 millions d'utilisateurs et environ 20 000 voitures disponibles dans le monde.

## II. Objectifs du projet
Ce projet vise à développer plusieurs applications clés :
- **Application d'Analyse des Retards** : Permet à l'équipe de GetAround de définir des seuils pour réduire les retards.
- **Application d'Entraînement de Modèles**: Pour prédire les prix de location des voitures en utilisant des techniques de machine learning.
- **API de Prévision des Prix de Location** : Permet aux utilisateurs de faire des requêtes pour obtenir des prédictions de prix de location de voitures.
## III. Structure du projet
Ce projet est structuré en deux sous-projets distincts, chacun avec son propre ensemble de codes sources et de fichiers README :
1- Analyse des retards (voir le code source et le README lien[])
2- Prédiction des prix de location de voiture (voir le code source et le fichier README lien[])

## IV. Livrables
- Un tableau de bord web dédié à l'analyse et aux simulations des retards : https://getearound-api-analysis-ac45266e0df6.herokuapp.com/
- Une application web hébergeant le serveur de suivi MLFlow : https://mlflow-api-85ae755d001e.herokuapp.com/
- Une API web pour les prévisions des prix de location de voitures : ???

## V. Auteur
Nene Oumou BARRY

# Tableau de bord : Analyse des données de Getaround 🚗

Lorsqu'un utilisateur retarde le retour d'une voiture louée sur GetAround, cela peut perturber la disponibilité du véhicule pour les locations suivantes, affectant ainsi la qualité du service et la satisfaction des clients. L'objectif ici est de déployer un tableau de bord en ligne pour aider GetAround à  non seulemrnt Évaluer l'ampleur du problème, mais aussi Simuler les conséquences potentielles de l'instauration d'un délai minimal entre deux locations consécutives d'un même véhicule sur l'entreprise. 

## Resultats
Vous pouvez accéder au tableau de bord en ligne à cet emplacement : https://getearound-api-analysis-ac45266e0df6.herokuapp.com/

## Exécution:
### I. Structure du projet
- **Dockerfile**: Ce fichier contient les instructions pour construire l'image Docker du projet.
- **app.py**: Ce fichier contient le code principal de l'application.
- **requirements.txt**: Ce fichier liste toutes les dépendances et versions nécessaires pour exécuter le projet.
- **README.md**: Ce fichier est la documentation principale du projet, fournissant des instructions d'installation, des exemples d'utilisation et d'autres informations pertinentes.

### II. Prérequis - Installations
* Avoir un éditeur de code (Visual Studio Code par exemple)
* Installer les packages requis
```bash
pip install -r requirements.txt
```
## II. Dossier du projet
Clonez ce dépôt pour créer votre dossier de projet :

`git clone https://github.com/nbarry96/ML-Supervis-.git`

## III. Créer et déployer l'appliation vers heroku

Placez-vous dans le répertoire du projet **Supervised_ML** 

```bash
cd delay-analysis
```

Créez l'application Heroku hébergeant l'application
```bash
heroku create <YOUR_APP_NAME>
```
Construire et faire un push de l'image Docker vers heroku
```bash
heroku container:push web -a <YOUR_APP_NAME>
```
Déployer l'image Docker vers heroku.
```bash
heroku container:release web -a <YOUR_APP_NAME>
```

## IV Source de données
Le jeu de données utilisé pour ce projet est fourni par Jedha Bootcamp et est disponible [ici](https://full-stack-assets.s3.eu-west-3.amazonaws.com/Deployment/get_around_delay_analysis.xlsx).

