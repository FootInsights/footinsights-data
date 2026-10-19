# FootInsights settled football predictions

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23471483.svg)](https://doi.org/10.5281/zenodo.23471483)

Every pre-match probability [FootInsights](https://footinsights.com) has
published since August 2026, settled against the final score. One row per
settled call: a market of a match (the model's 1X2, double chance,
over/under 1.5/2.5/3.5, both-teams-to-score and correct-score calls, and
the published tips), the call and what happened, the match's 1X2,
over 2.5 and BTTS probabilities, the model's public version name and the
settlement time. Append-only: nothing is edited or removed after
publication, misses included. Column reference: https://footinsights.com/data/

- Source and column reference: https://footinsights.com/data/
- Live file, refreshed with every pipeline run: https://footinsights.com/data/predictions.csv
- This repository: a weekly copy in [`data/predictions.csv`](data/predictions.csv) and a monthly release.
- Licence: [CC BY 4.0](LICENSE). Cite as in [`CITATION.cff`](CITATION.cff).
- Kaggle mirror, refreshed weekly: https://www.kaggle.com/datasets/footinsights/football-predictions-settled
- Brier score and reliability curve of the same rows, reproducible: https://www.kaggle.com/code/footinsights/notebook55d0cf9968
- DOI, all versions: [10.5281/zenodo.23471483](https://doi.org/10.5281/zenodo.23471483); each monthly release gets its own on Zenodo.

The track record and calibration of the same rows: https://footinsights.com/track-record/
