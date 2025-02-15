# PostgreSQL

Exercices avec postgreSQL similaires à ceux effectués avec Ducdbk

---

# Installation des dépendances et de l'environnement virtuel avec UV

**Attention, pour jupyter notebook, UV n'est pas adapté : installé au préalable l'environnement virtuel avec la fonctionnalité de VSC puis installer par la suite les dépendances avec UV**

**Création du projet à saisir dans le terminal** :

```
uv init
```

**Création d'un environnement virtuel, à saisir dans le terminal** :

```
uv venv
```

**Pour spécifier une version de python** :

```
uv venv --version 3.12
```

**Pour synchroniser l'environnement avec le nouveau fichier requirements.txt**

```
uv pip sync requirements.txt

```

Installation des dépendances :

```
uv add polars
```

Synchronisation de l'environnement :

```
uv sync
```

Qualité du code :

```
uvx ruff check # Analyse du colde
uvx ruff format # Formatage du code
uvx pytest # Lance les tests
```

---

# PostgreSQL

**Attention, selon le nom donné à la BD dans le terminal, lorsqu'on est dans l'instruction ci-après, on peut avoir un problème d'encodate utf-8 🤔 :**

```
metadata.create_all(engine)
```

Pour se connecter sur postgreSQL à partir du terminal, saisir :

```
psql -U postgres
```

Puis saisir le mot de passe pour l'accès à postgreSQL.

---

Pour voir les BD créées, saisir dans le terminal :

```
\l
```

---

Pour créer un nouvel utilisateur, saisir dans le terminal :

```
CREATE USER user WITH PASSWORD 'mot_de_passe';
```

(user = nom de l'utilisateur) <br>

---

Pour créer une nouvelle BD, saisir dans le terminal :

```
CREATE DATABASE nom_du_projet OWNER user;
```

---

Pour supprimer une BD, saisir dans le terminal :

```
DROP DATABASE nom_projet;
```

Pour créer un diagramme ERD (Entity-Relationship Diagram = Diagramme Entité-Relation), il faut au préalable installer l'application Graphviz avec l'option d'installation à la variable d'environnement PATH
