# Analysis on the Cessation Effect on Smoking among Patients with MDD with the Combination Treatment of Behavioral Activation and Varenicline

## Abstract

This study investigates the effectiveness of behavioral activation and varenicline for smoking cessation among individuals with current or past Major Depressive Disorder (MDD). Using data from a randomized, placebo-controlled, 2×2 factorial trial of 300 adult smokers, we employed regularized regression approaches (LASSO, Ridge, and Elastic Net) to examine treatment effects and their moderators. The analysis focused on identifying baseline characteristics that might influence treatment outcomes and exploring potential interactions between treatments and patient characteristics.

## Results

### Model Performance

| Model Type | Training AUC | Test AUC | Accuracy (Test) |
|------------|-------------|-----------|-----------------|
| LASSO | 0.841 | 0.705 | 0.808 |
| Ridge | 0.878 | 0.651 | 0.800 |
| Basic Interaction | 0.845 | 0.685 | 0.800 |
| Advanced Interaction | 0.854 | 0.711 | 0.808 |

### Plots

[](Figures/lasso_model.png)
[](Figures/advanced_interaction_variable_importance.png)

## Conclusions

1. Treatment Effectiveness
   - Varenicline shows robust positive effects across all models
   - Behavioral activation shows variable effects depending on patient characteristics

2. Treatment Effect Heterogeneity
   - Treatment effectiveness varies by smoking intensity and motivation
   - Socioeconomic factors significantly moderate treatment outcomes

3. Clinical Implications
   - Varenicline recommended as first-line treatment, especially for heavy smokers
   - Need for personalized treatment approaches considering both clinical and socioeconomic factors

## Repository Structure

```bash
smoke-cessation-effect-analysis
├── Data
│   ├── data_reformated.csv
│   └── project2.csv
├── Figures
│   ├── advanced_interaction_model.png
│   ├── advanced_interaction_variable_importance.png
│   ├── basic_interaction_model.png
│   ├── basic_interaction_variable_importance.png
│   ├── corr_plot.png
│   ├── dist_after_log.png
│   ├── dist_plot.png
│   ├── lasso_model.png
│   ├── lasso_variable_importance.png
│   ├── ridge_model.png
│   └── ridge_variable_importance.png
├── LICENSE
├── Outcomes.and.AE.Paper.Addiction.2023.pdf
├── README.md
└── Report
    ├── Report.Rmd
    └── Report.pdf
```