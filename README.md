# Healthcare Rates

A simple, notebook-first workspace for learning Python data science with the
healthcare rates CSV.

## Start here

Open a terminal in this folder and run:

```bash
uv run jupyter lab
```

In JupyterLab, open:

```text
notebooks/01_getting_started.ipynb
```

Run one cell at a time with **Shift+Enter**. Change things, rerun cells, and
experiment—that is exactly what the notebook is for.

## Project layout

```text
HealthcareRates/
├── data/          # Your input CSV
├── notebooks/     # Your analyses
├── artifacts/     # Charts or tables you save
├── pyproject.toml # The short list of installed libraries
└── uv.lock        # Exact versions, maintained automatically
```

The files beginning with a dot, such as `.venv`, `.gitignore`, and
`.python-version`, are setup files. You can generally leave them alone.

## What is installed

- `pandas`: data frames and data manipulation
- `numpy`: numerical computing
- `matplotlib` and `seaborn`: charts
- `scikit-learn`: machine learning
- `jupyterlab`: interactive notebooks

## Environment commands

```bash
uv run jupyter lab  # Start working
uv add plotly       # Install another library
uv sync             # Re-create the environment from the project files
```

You do not need to activate `.venv`; `uv run` uses it automatically.

## R-to-Python landmarks

| R / tidyverse | Python / pandas |
|---|---|
| `read_csv(path)` | `pd.read_csv(path)` |
| `head(df)` | `df.head()` |
| `glimpse(df)` | `df.info()` |
| `filter(df, x > 0)` | `df.loc[df["x"] > 0]` |
| `select(df, a, b)` | `df[["a", "b"]]` |
| `group_by(x) |> summarize(...)` | `df.groupby("x").agg(...)` |
| `is.na(x)` | `x.isna()` |
| `ggplot2` | `seaborn` / `matplotlib` |
