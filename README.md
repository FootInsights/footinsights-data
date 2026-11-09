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
- Hugging Face mirror, refreshed weekly: https://huggingface.co/datasets/footinsights/football-predictions-settled
- Brier score and reliability curve of the same rows, reproducible: https://www.kaggle.com/code/footinsights/notebook55d0cf9968
- DOI, all versions: [10.5281/zenodo.23471483](https://doi.org/10.5281/zenodo.23471483); each monthly release gets its own on Zenodo.

The track record and calibration of the same rows: https://footinsights.com/track-record/

Browse the matches behind these rows by competition:
[Premier League](https://footinsights.com/leagues/premier-league/),
[Championship](https://footinsights.com/leagues/championship/),
[League One](https://footinsights.com/leagues/league-one/),
[La Liga](https://footinsights.com/leagues/la-liga/),
[MLS](https://footinsights.com/leagues/mls/) and
[Liga MX](https://footinsights.com/leagues/liga-mx/).
Tips published from the same model before kick-off, such as the
[Daily Double](https://footinsights.com/tips/daily-double/) and the
[Bankers](https://footinsights.com/tips/bankers/), settle into this file too.

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
| `market` | string | Market. The model's calls: 1x2, dc (double chance), ou15/ou25/ou35 (over/under 1.5/2.5/3.5), btts, cs (correct score). The published tips: result, goals and both (the three tips frozen per match with their price), best (the Best Tip), banker and value (the Value Bet, a product retired on 4 November 2026; its settled rows stay, as every row does). |
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
