# README

## Projet Python ISDS1 2024

### Présentation Générale

Ce projet a été réalisé dans le cadre du cours ISDS1 à l'ISUP entre février et avril 2024. L'objectif du projet est d'appliquer les outils et méthodes vus en cours pour analyser des jeux de données et construire des modèles linéaires. Le projet se divise en deux parties principales :

1. Analyse statistique et modèle linéaire
2. Calculateur d'empreinte carbone

Ce document se concentre sur la partie 2 : calculateur d'empreinte carbone.

### Partie 2 : Calculateur d'empreinte carbone

#### 2.1 Jeu de Données

Le jeu de données utilisé pour cette partie provient de la base de données carbone, contenant des informations sur les émissions de CO2 par poste de consommation.

#### 2.2 Objectifs

L'objectif principal de cette partie est de développer un calculateur d'empreinte carbone capable de :
- Calculer les émissions de CO2 en fonction des consommations données.
- Afficher les résultats des émissions de CO2.
- Calculer les émissions de CO2 par catégorie en fonction des consommations données.

### Modules et Fonctions

#### Module `CalcuCarbone.py`

**Classe `CarbonCalculator`**:
- `__init__(self, data)`: Initialise le calculateur d'empreinte carbone avec les données fournies. Le paramètre `data` est un `pandas.DataFrame` contenant les données d'émission de CO2.
- `calculer_emissions(self, consommations)`: Calcule les émissions de CO2 en fonction des consommations données. Le paramètre `consommations` est un dictionnaire contenant les consommations par poste. La fonction retourne un dictionnaire des émissions par catégorie.
- `convertir_frequence(consommation, frequence)`: Convertit la consommation en consommation annuelle. Le paramètre `frequence` peut être 'q' pour quotidienne, 'h' pour hebdomadaire, 'm' pour mensuelle, ou 'a' pour annuelle.
- `afficher_resultats(self, consommations)`: Affiche les résultats des émissions de CO2. Le paramètre `consommations` est un dictionnaire contenant les consommations par poste.
- `calculer_emissions_par_categorie(self, consommations, categories)`: Calcule les émissions de CO2 par catégorie en fonction des consommations données. Le paramètre `categories` est un dictionnaire des catégories et sous-catégories. La fonction retourne un dictionnaire des émissions par catégorie.

#### Module `main.py`

**Fonction `main()`**:
- Fonction principale qui exécute les différentes fonctions et méthodes du projet. Elle lit les fichiers CSV contenant les données, initialise le calculateur d'empreinte carbone, demande à l'utilisateur sa consommation annuelle par catégorie, calcule et affiche les résultats des émissions de CO2, et génère un graphique des émissions par catégorie.

#### Module `loading.py`

**Fonction `lecture2(fichier)`**:
- Charge le fichier CSV et retourne un `pandas.DataFrame` contenant les données chargées. Le paramètre `fichier` est le chemin vers le fichier CSV. La fonction gère également les valeurs manquantes en les remplaçant par des valeurs par défaut (0 pour les valeurs numériques et des chaînes vides pour les chaînes de caractères).

### Installation et Utilisation

Pour utiliser ce calculateur d'empreinte carbone, suivez ces étapes :

1. Clonez le dépôt ou téléchargez les fichiers du projet.
2. Installez les dépendances nécessaires listées dans le fichier `setup.py`.
3. Exécutez le module `main.py` pour démarrer le calculateur et suivre les instructions à l'écran pour entrer vos consommations annuelles par catégorie.
4. Visualisez les résultats des émissions de CO2 par catégorie.
5. En cas d'obtention de résultats non cohérents avec la réalité, voir le dossier `exemple_application` où les valeurs entrées dans chaques catégories sont précisées dans le fichier .txt et le graphique résultat joint en fichier .png 

### Auteur

Erivan INAN

