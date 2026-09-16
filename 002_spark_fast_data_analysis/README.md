# 002 — Spark: szybka analiza danych

Notatnik `002_spark_fast_data_analysis.ipynb` oraz towarzyszące mu skrypty (`002A_*.py`, `002B_*.py`)
i notatniki referencyjne w `Databricks/` bazują na materiałach z książki
[*Learning Spark, 2nd Edition*](https://www.oreilly.com/library/view/learning-spark-2nd/9781492050032/)
i jej repozytorium [databricks/LearningSparkV2](https://github.com/databricks/LearningSparkV2)
(Apache License 2.0).

## Dane

Dwa duże, surowe zbiory danych z tego repozytorium **nie są** wersjonowane w git (74 MB łącznie) —
patrz `.gitignore`. Żeby uruchomić notatnik lokalnie, pobierz je do tego folderu:

```bash
curl -o 002B_sf-fire-calls.csv \
  https://raw.githubusercontent.com/databricks/LearningSparkV2/master/databricks-datasets/learning-spark-v2/sf-fire/sf-fire-calls.csv

curl -o 002C_departuredelays.csv \
  https://raw.githubusercontent.com/databricks/LearningSparkV2/master/databricks-datasets/learning-spark-v2/flights/departuredelays.csv
```

Pozostałe, mniejsze pliki (`002A_mnm_dataset.csv`, `002B_blogs.json`) zostają w repo — są małe i generowane/używane bezpośrednio przez notatnik.

## Databricks/

Ten podfolder to niezmodyfikowana kopia oficjalnych notatników kursowych Databricks Academy
(rozdziały 2–5 książki), dołączona jako materiał referencyjny — kod celowo zostawiony
w oryginalnym, angielskim brzmieniu (wraz z literówkami autorów), żeby zachować wierność źródłu.
