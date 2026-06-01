# Lab 15 — SQLite et Android : Gestion simple des étudiants

Ce projet Android illustre l'utilisation de **SQLite** pour stocker et gérer des données localement sur l'appareil, sans connexion réseau. L'application permet d'ajouter, rechercher et supprimer des étudiants dans une base de données embarquée.

---

## Fonctionnalités

- Ajouter un étudiant (nom + prénom)
- Rechercher un étudiant par son ID
- Supprimer un étudiant par son ID

---

## Architecture

- **`Etudiant`** : classe modèle représentant un étudiant
- **`MySQLiteHelper`** : gère la création et la mise à jour de la base de données SQLite
- **`EtudiantService`** : contient toutes les opérations CRUD (create, findById, delete, update, findAll)
- **`MainActivity`** : interface utilisateur, relie les boutons aux actions du service

---

## Base de données

La base s'appelle `ecole` et contient une table `etudiant` :

```sql
CREATE TABLE etudiant (
    id      INTEGER PRIMARY KEY AUTOINCREMENT,
    nom     TEXT,
    prenom  TEXT
);
```

---

## Aperçu

> Les captures ci-dessous montrent l'ajout et la recherche d'un étudiant dans l'application.
> <img width="218" height="506" alt="image" src="https://github.com/user-attachments/assets/84f099c3-6f2e-45ae-be3c-1d5d8272da0c" />
<img width="241" height="517" alt="image" src="https://github.com/user-attachments/assets/3feb56b1-c925-4d41-9cb7-d2c94bf45254" />
