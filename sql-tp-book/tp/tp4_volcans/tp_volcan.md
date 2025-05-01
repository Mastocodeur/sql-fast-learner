# TP SQL Volcans
## Présentation et contexte

Vous travaillez pour une organisation scientifique qui répertorie les volcans actifs et souhaite analyser certaines caractéristiques de ces volcans.

Vous disposez d'une base de données sur les volcans `volcans.db` qui contient des informations géographiques, historiques et encyclopédiques sur des volcans du monde entier. Chaque ligne représente un volcan et vous informe sur : 

* `volcano` : Lien vers le site source
* `name` : Le nom du volcan
* `wiki` : La page wikipedia du volcan
* `elevation` : La hauteur du volcan (altitude)
* `lat` : La latitude 
* `lon` : La longitude
* `eruption_date` : La date d'éruption du volcan
* `eruption_year` : L'année d'éruption du volcan
* `abstract` : Une description détaillée, parfois historique, du volcan.
* `photo` : Un lien vers une image (souvent issue de Wikimedia Commons).

## Objectifs de ce TP
1. Apprendre à manipuler des données géographiques et temporelles.

2. Utiliser des requêtes SQL pour filtrer, agréger et ordonner les données.

## Enoncé du TP

### Partie 1 – Exploration de la base 
1) Lister les 10 volcans les plus hauts, classés par altitude décroissante.

2) Trouver les volcans dont l’altitude est supérieure à 5000 mètres.

3) Afficher le nom, l'altitude et le lien Wikipédia pour les volcans ayant une altitude non nulle.

### Partie 2 – Analyse temporelle
4) Lister les volcans ayant eu une éruption après l’an 2000.

5) Trouver combien de volcans ont une année d’éruption connue (c’est-à-dire non nulle).

6) Trier les volcans par année d’éruption décroissante (les plus récents d'abord).

### Partie 3 – Données géographiques

7) Trouver les volcans situés dans l’hémisphère sud.

8) Compter le nombre de volcans situés entre l’équateur (lat = 0) et 30°N.

9) Identifier les 5 volcans les plus au nord (par latitude décroissante).

### Partie 4 – Requête avancée (bonus)
10) Extraire les volcans ayant dans leur description (abstract) le mot "eruption".