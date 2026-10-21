---
license: cc-by-4.0
language:
  - en
pretty_name: FootInsights settled football predictions
tags:
  - football
  - soccer
  - sports
  - forecasting
  - betting
  - calibration
  - model-evaluation
size_categories:
  - 10K<n<100K
configs:
  - config_name: default
    data_files: predictions.csv
---

# FootInsights settled football predictions

Every pre-match probability [FootInsights](https://footinsights.com) has
published since August 2026, settled against the final score. One row per
settled call: a market of a match (the model's 1X2, double chance,
over/under 1.5/2.5/3.5, both-teams-to-score and correct-score calls, and the
published tips), the call and what happened, the match's 1X2, over 2.5 and
BTTS probabilities, the model's public version name and the settlement time.
Append-only: nothing is edited or removed after publication, misses included.

- Column reference: https://footinsights.com/data/
- Live file, refreshed with every pipeline run: https://footinsights.com/data/predictions.csv
- Source repository, weekly copy and monthly release: https://github.com/FootInsights/footinsights-data
- DOI, all versions: [10.5281/zenodo.23471483](https://doi.org/10.5281/zenodo.23471483)
- Kaggle mirror: https://www.kaggle.com/datasets/footinsights/football-predictions-settled
- Track record and calibration of the same rows: https://footinsights.com/track-record/

This mirror is refreshed every Monday from the live file.

## Citation

FootInsights (2026). FootInsights settled football predictions. Zenodo.
https://doi.org/10.5281/zenodo.23471483

## Licence

CC BY 4.0. A credit and a link back are all we ask.
