# ecommerce-analytics

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Pandas](https://img.shields.io/badge/Pandas-Yes-green)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## Description

Pipeline d’analyse de données e-commerce : extraction, nettoyage, enrichissement et agrégation pour générer des KPI quotidiens et mensuels.

**Étapes principales :**

* Extraction depuis Google Drive & SQLite
* Nettoyage (doublons, valeurs manquantes)
* Enrichissement (calcul du chiffre d’affaires)
* Agrégation (KPI journaliers & mensuels)

## Installation rapide

```bash
git clone <URL_DU_PROJET>
cd ecommerce-analytic
python -m venv env
source env/bin/activate   # Linux/Mac
env\Scripts\activate      # Windows
pip install -r requirements.txt
```

## Utilisation

bash
cd dags/common
python extract.py     # Extraction
python transform.py   # Nettoyage
python enrich.py      # Enrichissement
python aggregate.py   # Agrégation


## KPI produits

* Clients uniques (quotidien)
* Stock disponible (quotidien)
* Chiffre d’affaires (mensuel)

## Dépendances

Python 3.11, pandas, google-api-python-client, google-auth

## Bonnes pratiques

* Respecter la structure année/mois/jour pour tous les fichiers.

* Vérifier la présence du fichier Service Account JSON avant toute exécution.

* Lancer les scripts dans l’ordre :
extract.py → transform.py → enrich.py → aggregate.py.
