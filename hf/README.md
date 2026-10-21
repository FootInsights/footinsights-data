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

## Columns

One row per settled call. Fields can be empty where a value was never recorded.

| Column | Type | Meaning |
| --- | --- | --- |
| `kickoff_utc` | datetime | Kick-off time, ISO 8601, UTC. |
| `league` | string | Competition name, e.g. Premier League. |
| `home_team` | string | Home team, full name. |
| `away_team` | string | Away team, full name. |
| `home_goals` | integer | Full-time home goals. |
| `away_goals` | integer | Full-time away goals. |
| `market` | string | Market. The model's calls: 1x2, dc (double chance), ou15/ou25/ou35 (over/under 1.5/2.5/3.5), btts, cs (correct score). The published tips: result, goals and both (the three tips frozen per match with their price), best (the Best Tip), banker and value (the Value Bet). |
| `predicted` | string | Our call: home/draw/away, 1X/12/X2, over/under, yes/no, a scoreline, or market/selection for best and banker. |
| `actual` | string | What happened, same vocabulary as predicted. |
| `correct` | boolean | true when the call matched the outcome. |
| `p_home` | number | Published probability of a home win (0-1). |
| `p_draw` | number | Published probability of a draw (0-1). |
| `p_away` | number | Published probability of an away win (0-1). |
| `p_over25` | number | Published probability of over 2.5 goals (0-1). |
| `p_btts` | number | Published probability of both teams scoring (0-1). |
| `confidence` | number | Model confidence in the main pick (0-1). |
| `model_version` | string | Public name of the FootInsights model version that priced the match (e.g. v3.1); blank where a version has no public name. |
| `settled_at` | datetime | When the prediction was settled, ISO 8601, UTC. |
| `match_url` | string | Permanent URL of the match's prediction page. |

## Scoring it

A public Kaggle notebook scores the same rows (Brier score and reliability
curve): https://www.kaggle.com/code/footinsights/notebook55d0cf9968

## Citation

FootInsights (2026). FootInsights settled football predictions. Zenodo.
https://doi.org/10.5281/zenodo.23471483

```bibtex
@dataset{footinsights_settled_predictions_2026,
  author    = {FootInsights},
  title     = {FootInsights settled football predictions},
  year      = {2026},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.23471483},
  url       = {https://doi.org/10.5281/zenodo.23471483}
}
```

## Licence

CC BY 4.0. A credit and a link back are all we ask.
