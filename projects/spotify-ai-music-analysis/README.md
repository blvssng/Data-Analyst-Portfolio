# Spotify and AI-Generated Music Analysis

An exploratory data analysis project investigating music streaming trends, track popularity, and the potential business implications of AI-generated music for Spotify. The project will combine audio-feature and engagement analysis with publicly reported financial data to connect listener and music trends with Spotify's commercial performance.

> **Project status:** Planned / in progress. Findings, charts, and model results will be added after the analysis has been completed. This README describes the research plan, not completed results.

## Type of Analysis

**Primary approach: Descriptive analysis.**

This project asks which audio features are associated with popular tracks, how top-charting songs have changed over the past 10–20 years, and how Spotify's subscriber growth compares with its revenue. These questions can be explored by summarising historical data. I will use measures such as averages and distributions, trends over time, and comparisons across genres and years to describe what has happened in the data.

Some parts of the project may extend beyond description:

- **Diagnostic analysis** can help investigate possible reasons behind observed patterns—for example, why some genres grew or why certain audio features are associated with popularity. These relationships will be treated as observational, not proof of cause and effect.
- **Predictive analysis** applies to the AI-generated music question, where I plan to evaluate a simple classifier that predicts whether a track is labelled AI-generated or human-made.

Descriptive analysis is the foundation of the project, with diagnostic and predictive methods serving as extensions.

## Research Questions

### Music and audio trends

- Which audio features—such as danceability, energy, tempo, and valence—are associated with track popularity in the available datasets?
- How have charting tracks and their characteristics, including track length, changed over the past 10–20 years?
- Which genres appear to have grown or declined over time?
- Can tracks be grouped into interpretable mood clusters using their available audio features?

### Listening behaviour

- How does listening vary by time of day, day of the week, or season, where timestamped listening data is available?
- Which playlists and genres account for the most streams in the selected dataset?
- How do South African genres, including amapiano, compare with broader trends represented in the data?

### Business and finance

- How do Spotify's reported subscriber and revenue growth compare over time?
- How do premium subscriber trends relate to quarterly revenue, operating costs, margins, and profitability?
- What public evidence is available about music streaming payouts across markets and subscription tiers?

### AI-generated music

- What share of tracks is labelled AI-generated in the selected labelled sample, and how does that share change over time if dates are available?
- How do labelled AI-generated and human-made tracks compare on available audio features and engagement measures?
- How well can a baseline classifier distinguish the two labels, measured with accuracy, precision, recall, and F1 score?

### Annotation and label quality

- How consistently do annotators agree on categorical labels such as genre or mood, when multiple independent annotations are available?
- Where appropriate, how do human-provided labels compare with categories derived from audio features?

## Data Sources

The analysis may use the following public sources, subject to availability, licensing, and access restrictions:

- Public Spotify track and audio-feature datasets, including relevant Kaggle datasets.
- The Spotify Web API, if the required data and endpoints are available under the API's current policies and restrictions.
- Spotify investor-relations materials and quarterly financial reports.
- Public or research datasets containing AI-generated music labels.

The final project will document each dataset's source, collection date, licence or terms of use, coverage, label definitions, and any transformations. For labelled AI-generated music data, it will also describe how the sample was assembled and its size. No private, confidential, or restricted professional data will be used.

## Tools and Technologies

- **Python:** pandas, scikit-learn, matplotlib (and other libraries as needed)
- **SQL:** data querying and analysis
- **Power BI or Tableau:** dashboards and visualisation
- **Git and GitHub:** version control and documentation

## Planned Workflow

1. Identify suitable public datasets and review their licences, terms, and limitations.
2. Load, profile, clean, and document the data.
3. Explore trends in track features, genres, engagement, and available listening behaviour.
4. Analyse Spotify's publicly reported financial and subscriber metrics separately, then compare trends over time where periods are comparable.
5. Build visualisations and, if the labelled sample is sufficient, evaluate a baseline AI-versus-human classifier using an appropriate held-out test set.
6. Interpret results, document limitations, and summarise potential business implications.

## Planned Repository Structure

```text
spotify-ai-music-analysis/
├── README.md
├── data/          # data documentation; raw data may be excluded from Git
├── notebooks/     # exploration and analysis
├── src/           # reusable cleaning and analysis scripts
└── dashboard/     # Power BI or Tableau files
```

Datasets will only be committed when their licences and size permit it. Otherwise, the repository will include instructions for obtaining the data and the steps needed to reproduce the analysis.

## Evaluation and Interpretation Notes

- Audio-feature and popularity relationships are observational and should not be presented as evidence that one feature causes popularity.
- Results depend on the coverage, definitions, and biases of the selected datasets; a public track sample may not represent all Spotify listeners or markets.
- Financial metrics will be taken from dated public reports, with definitions and reporting periods recorded to support fair comparisons.
- Classifier performance will be reported alongside class balance and the evaluation method. A high score on one labelled sample does not establish that the model generalises to all AI-generated music.
- Cohen's kappa is appropriate for agreement between independent annotators assigning comparable categorical labels. It does not directly measure agreement between a human label and a continuous audio feature; any such comparison will use a clearly defined, suitable method instead.
- Streaming payouts vary with rights, contracts, markets, and other factors. Public information may not support a reliable direct comparison across all markets or subscription tiers.

## Findings

*To be added after the analysis is complete.*

## About

**Blessing Muchirahondo** — data professional based in Johannesburg, South Africa.
