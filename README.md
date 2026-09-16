# pyspark-lab

Notatniki i skrypty z nauki PySparka — od podstaw DataFrame API, przez schematy, joiny,
agregacje i UDF-y, po Spark SQL i przykłady end-to-end na realnych zbiorach danych.

Repozytorium powstawało jako materiał do nauki (2024), teraz uporządkowane i opublikowane
jako punkt odniesienia — dla siebie i dla każdego, kto zaczyna z PySparkiem.

## Struktura

| Folder | Zawartość |
|---|---|
| [`000_Setup_PySpark_+_GIT.ipynb`](000_Setup_PySpark_+_GIT.ipynb) | Środowisko: obraz Docker `jupyter/all-spark-notebook`, pierwszy setup repo w Git |
| [`001_data_processing_and_analysis_in_etl_processes/`](001_data_processing_and_analysis_in_etl_processes/) | Podstawy DataFrame API: wczytywanie CSV, schematy, selekcja, filtrowanie, grupowanie, joiny, UDF-y, zapis do parquet, Spark SQL |
| [`002_spark_fast_data_analysis/`](002_spark_fast_data_analysis/) | Szybka analiza danych: generowanie i agregacja datasetu M&M, źródła danych (CSV/JSON/Parquet/Avro/ORC), Spark SQL na przykładzie lotniczych opóźnień (PIVOT, window functions) — plus `Databricks/`, referencyjne notatniki z kursu *Learning Spark, 2nd Edition* |
| [`003_eda_ecommerce_data_mining/`](003_eda_ecommerce_data_mining/) | EDA na [zbiorze transakcji e-commerce z Kaggle](https://www.kaggle.com/datasets/carrie1/ecommerce-data): przychody, sezonowość, segmentacja klientów |
| [`004_pyspark_recipes/`](004_pyspark_recipes/) | Krótkie, samodzielne przykłady: accumulator, partycjonowanie i zapis (`coalesce` vs `repartition`), `union`/`unionByName`, `explode`/`posexplode`, `pivot`/`unpivot`, `withColumn` |

## Uruchomienie

Wymagany PySpark (i Jupyter). Najprościej przez obraz Dockera opisany w
[`000_Setup_PySpark_+_GIT.ipynb`](000_Setup_PySpark_+_GIT.ipynb):

```bash
docker pull jupyter/all-spark-notebook
docker run -p 8888:8888 -v "$(pwd)":/home/jovyan/work jupyter/all-spark-notebook
```

Alternatywnie lokalnie: `pip install pyspark jupyter` i uruchom notatniki bezpośrednio.

Duże, surowe zbiory danych używane w `002_spark_fast_data_analysis/` nie są wersjonowane w repo —
instrukcja pobrania w [`002_spark_fast_data_analysis/README.md`](002_spark_fast_data_analysis/README.md).

## Licencja

Własna zawartość repozytorium — [MIT](LICENSE).

Podfolder `002_spark_fast_data_analysis/Databricks/` to niezmodyfikowana kopia oficjalnych
notatników kursowych [databricks/LearningSparkV2](https://github.com/databricks/LearningSparkV2),
licencjonowana osobno na [Apache License 2.0](002_spark_fast_data_analysis/Databricks/LICENSE).
