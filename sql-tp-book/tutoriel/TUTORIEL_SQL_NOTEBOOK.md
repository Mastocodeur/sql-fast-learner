# 📘 Faire du SQL dans un notebook Jupyter avec ipython-sql


Cette page explique comment exécuter des requêtes SQL directement dans un notebook Jupyter, sans sortir de l’environnement Python, grâce à l’extension magique `ipython-sql`.

## ⚙️ Installation de l’environnement

➤ Installer Anaconda (inclut Python + Jupyter):

1. Va sur https://www.anaconda.com/download

2. Télécharge l’installateur adapté à ton système (Windows, macOS ou Linux)

3. Installe Anaconda en suivant les instructions

## 📦 Installation du module ipython-sql

Une fois Jupyter installé, ouvrir un terminal (ou Anaconda Prompt) et installer le module avec la commande :

```bash
pip install ipython-sql
```

On peut aussi l’installer depuis une cellule Jupyter en tapant :

```python
!pip install ipython-sql
```

## 🧰 Utilisation de `ipython-sql` dans un notebook

Pour activer le mode SQL dans un notebook, on commence par charger l’extension magique :

```python
%load_ext sql
```
Ensuite, on se connecte à une base SQLite (ou autre) en utilisant une URI. Par exemple, pour une base locale `ma_base.db` (présente dans nos fichiers donc), on utilisera la commande :

```python
%sql sqlite:///ma_base.db
```

Si la base de données est dans un fichier, il faudra évidemment changer l'URI. Si tout s'est bien passé, la cellule s'éxécute sans erreurs.

On peux maintenant écrire du SQL directement dans une cellule en commençant par %%sql, exemple:

```python
%%sql
SELECT *
FROM utilisateurs
WHERE age > 30
```

Le résultat s’affiche directement sous forme de tableau interactif dans le notebook.


## 💡 Astuces

Quelques astuces : 
* `%%sql` au début d’une cellule permet d’écrire plusieurs lignes de SQL

* `%sql` permet d’exécuter une requête en ligne simple

On peut utiliser des variables Python dans une requête SQL avec `:nom_variable`

