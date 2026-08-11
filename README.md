# Analyse des Données du Titanic — Data Mining

Master 2 Informatique de Gestion | UCAO Dakar
Auteur : Mahamat Haroun Ibrahim

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=flat)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat&logo=scipy)

## Objectifs

- Charger et explorer les données du Titanic
- Nettoyer et préparer les données
- Visualiser les relations entre les variables
- Appliquer des tests statistiques pour valider des hypothèses

## Dataset

891 passagers, 13 colonnes d'origine (identifiant, classe, nom, genre, âge, liens familiaux, billet, tarif, cabine, port d'embarquement, survie).

## Méthodologie

**1. Exploration** — structure des données, statistiques descriptives (âge moyen 29 ans, taux de survie global 38%).

**2. Nettoyage**
- Renommage de `Sex` en `Genre`
- Suppression des colonnes non pertinentes pour l'analyse (`SibSp`, `Parch`, `Ticket`, `Fare`)
- Valeurs manquantes : `Age` (19.9%) imputé par la médiane, `Embarked` (0.2%) imputé par le mode, `Cabin` (77.1% manquant) supprimée

**3. Visualisation** — répartition des survivants, taux de survie par genre, par âge, par classe sociale.

**4. Test statistique** — test du Khi-2 sur l'association Genre × Survie.

## Résultats clés

| Variable | Impact sur la survie | Observation |
|---|---|---|
| Genre | Significatif (Khi-2 = 260.72, p < 0.001) | Les femmes ont survécu en plus grande proportion (72% vs 19% pour les hommes) |
| Classe | Significatif | Les passagers de 1ère classe ont un taux de survie plus élevé |
| Âge | Modéré | Les enfants ont été priorisés lors de l'évacuation |

**Conclusion** : la survie n'était pas aléatoire. Le test du Khi-2 confirme statistiquement que le genre influence significativement les chances de survie (p-value < 0.05, H0 rejetée).

## Stack technique

Python · pandas · numpy · matplotlib · seaborn · scipy (test du Khi-2)

## Utilisation

```bash
pip install pandas numpy matplotlib seaborn scipy
jupyter notebook Analyse_Titanic.ipynb
```
