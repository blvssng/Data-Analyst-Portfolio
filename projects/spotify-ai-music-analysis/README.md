# Spotify and AI-Generated Music Analysis

An exploratory analysis of AI-generated music, focused on how labelled AI-generated tracks compare with human-made tracks and how reliably a baseline model can distinguish between them. The project will use publicly available datasets and document their coverage, labels, and limitations.

> **Project status:** Planned / in progress. Findings, charts, and model results will be added after the analysis has been completed. This README describes the research plan, not completed results.

## Type of Analysis

**Primary approach: Descriptive analysis, with a predictive modelling extension.**

The project will describe the labelled sample and compare AI-generated and human-made tracks using available audio features and engagement measures. If the data is suitable, a baseline classifier will be evaluated to predict the labels. Model performance will be treated as evidence about the selected dataset—not proof that a model can reliably identify all AI-generated music.

## Research Questions

- What share of tracks in the dataset is labelled as AI-generated, and how does that share vary over time where dates are available?
- What audio characteristics are most common among AI-generated tracks in the selected dataset?
- How do AI-generated tracks differ from human-made tracks on features such as danceability, energy, tempo, and valence?
- Which patterns in AI-generated music are associated with higher engagement or popularity where such data is available?
- How accurately can a baseline classifier identify AI-generated tracks using available audio features and metadata?

## Data Sources

The analysis may use public or research datasets containing AI-generated music labels, subject to availability, licensing, and access restrictions. Track metadata, audio features, and engagement measures will only be included where they are available and their use is permitted.

The final project will document each dataset's source, collection date, licence or terms of use, coverage, label definitions, and any transformations. It will distinguish dataset-provided labels from labels independently verified by the project, if applicable.

## Tools and Technologies

- **Python:** pandas, scikit-learn, matplotlib (and other libraries as needed)
- **SQL:** data querying and analysis
- **Git and GitHub:** version control and documentation

## Planned Workflow

1. Identify suitable public datasets and review their licences, terms, label definitions, and limitations.
2. Load, profile, clean, and document the data, including missing values and class balance.
3. Compare AI-generated and human-made tracks using the audio features and engagement measures available in the selected dataset.
4. Create visualisations that describe the sample and highlight group differences without implying causation.
5. If the labelled sample is sufficient, train and evaluate a baseline classifier using an appropriate held-out test set; report accuracy, precision, recall, and F1 score alongside class balance.
6. Interpret the results, document limitations, and summarise what the data can and cannot establish.

## Planned Repository Structure

```text
spotify-ai-music-analysis/
├── README.md
├── data/          # data documentation; raw data may be excluded from Git
├── notebooks/     # exploration and analysis
├── src/           # reusable cleaning and analysis scripts
└── dashboard/     # visualisations, if useful
```

Datasets will only be committed when their licences and size permit it. Otherwise, the repository will include instructions for obtaining the data and the steps needed to reproduce the analysis.

## Evaluation and Interpretation Notes

- Results depend on the coverage, definitions, and biases of the selected datasets; a labelled sample may not represent the wider range of AI-generated or human-made music.
- Differences in audio features or engagement are observational and should not be presented as evidence that AI generation causes those differences.
- Classifier performance will be reported alongside class balance, the evaluation method, and relevant limitations. A high score on one labelled sample does not establish that the model generalises to new datasets, genres, or AI-generation methods.
- Data leakage will be considered when splitting data, particularly where multiple tracks by the same artist or related versions of a track could appear in both training and test sets.
- Label quality and the method used to assign AI-generated or human-made labels will be documented. Uncertain or inconsistent labels may affect comparisons and model performance.

## Findings

*To be added after the analysis is complete.*

## About

**Blessing Muchirahondo** — data professional based in Johannesburg, South Africa.
