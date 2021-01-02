# Bachelor's Degree Research

## Разработка

Для установки зависимостей воспользуейтесь командой:
```bash
conda create --name <env> --file requirements.txt
```

Для создания директорий с данными и их загрузки:
```bash
snakemake data --cores 1
```

На данный момент также требуется установить переменную окружения `DP_PROJECT_PATH`
в путь до директории данного проекта.

## Языковые модели

Можно взять уже обученные в ноутбуке `3.0-db-training_lm.ipynb` языковые модели по ссылке: [тут будет ссылка]().

Если требуется обучить языковые модели на своем корпусе, то потребуется склонировать [kenlm]() в src/kenlm и скомпилировать библиотеку, а потом повторить то, что было сделано в ноутбуке `3.0-db-training_lm.ipynb`.


## Структура проекта

------------

    ├── Snakefile           <- Snakefile with commands like `snakemake data` or `snakemake train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- Documentation for the project
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `conda list -e > requirements.txt`
    │
    └── src                <- Source code for use in this project.
        ├── __init__.py    <- Makes src a Python module
        │
        ├── models         <- Models classes
        │
        ├── configs        <- Configurations of pipelines 
        │
        └── utils          <- Useful functions and classes for all project
