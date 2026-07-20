# Democratic Voter Shift in Pennsylvania

County-level analysis of Democratic vote-share change, turnout dynamics, and demographic predictors in Pennsylvania elections.

## Overview

This project analyzes county-level Democratic vote-share change across Pennsylvania to identify where the party lost ground, whether those losses were driven more by turnout decline or persuasion loss, and how far demographic structure helps explain geographic variation in those shifts. The analysis combines official election returns, American Community Survey demographic indicators, and Ridge regression modeling in a reproducible Python workflow.[1][2][3]

In addition to descriptive mapping and ranked county comparisons, the project evaluates whether county-level Democratic decline was broadly statewide or concentrated in specific geographic and demographic contexts. A later extension also explored adding issue-based text measures, though the strongest reported results come from the demographics-focused model.[1][4][5][6]

## Research Questions

1. Which Pennsylvania counties experienced the largest shifts away from the Democratic Party?[1]
2. To what extent were those shifts driven by turnout decline versus persuasion loss?[1]
3. How much of county-level variation in Democratic vote-share change can be explained by demographic characteristics?[2][3]

## Key Findings

- The largest Democratic declines were not uniform across the state; they were concentrated in specific counties rather than evenly distributed statewide.[1]
- The project distinguishes turnout effects from persuasion effects rather than treating raw vote-share change as a single mechanism.[1]
- In the demographics-only Ridge model, county characteristics explained a meaningful share of variation in Democratic vote-share change, with in-sample R² = 0.569, LOOCV R² = 0.479, and LOOCV RMSE = 0.00721.[3]
- The text-based extension did not materially improve model performance beyond the demographic baseline in its current form.[6]

## Selected Visuals


*Figure 1. County vote-shift choropleth.*
<img width="2385" height="1810" alt="pa_county_democratic_shift" src="https://github.com/user-attachments/assets/2624055a-7a81-4365-9a4d-43c317930177" />

*Figure 2. County-level turnout choropleth map.*
<img width="2850" height="2108" alt="pa_county_turnout_change" src="https://github.com/user-attachments/assets/14c5dc65-2381-4b52-9908-a33414e08c98" />

*Figure 3. Turnout-versus-persuasion visual.*
<img width="1400" height="1050" alt="persuation" src="https://github.com/user-attachments/assets/164d449e-81f9-4815-9453-36d3ea07a513" />

*Figure 4. Coefficient plot or model-results figure.*
<img width="750" height="420" alt="ridge_q3_coefficients" src="https://github.com/user-attachments/assets/00c376d2-617b-4b80-babb-64d0916834ca" />


## Data Sources

- Pennsylvania county-level election returns.[1]
- American Community Survey demographic variables, including measures such as educational attainment, income, poverty, unemployment, racial composition, and foreign-born share.[2][3]
- Experimental text-based issue measures explored later in the project workflow.[9][5][6]

## Methods

- Data cleaning and county-level merging in Python.[2]
- Descriptive ranking, mapping, and comparative visual analysis of county shifts.[1]
- Ridge regression to model county-level Democratic vote-share change while handling multicollinearity in a small-
  sample setting.[2][3]
- Leave-one-out cross-validation to evaluate generalization performance.[3]

## Repository Structure

```text
democratic-voter-shift/
├── README.md
├── requirements.txt
├── data/
│   ├── raw/
│   ├── processed/
│   └── data_dictionary.md
├── notebooks/
├── src/
├── outputs/
│   ├── figures/
│   ├── tables/
│   └── model_results/
└── paper/
    └── democratic_voter_shift_paper.pdf
```

This structure follows common GitHub portfolio and research-repository guidance: keep the README as the entry point, separate raw and processed data, isolate analysis code, and store final figures and manuscript outputs in clearly named folders.[10][11][12][13]

## Reproducibility

To reproduce the analysis:

1. Clone the repository.
2. Install the dependencies in `requirements.txt`.
3. Place raw election and demographic data in the `data/raw/` directory.
4. Run the cleaning, merge, and analysis scripts or notebooks in the documented order.
5. Save figures, tables, and model outputs to `outputs/`.

If some source files cannot be redistributed publicly, note that clearly in the repository and explain how reviewers can still understand the workflow without direct access to those files.[8][10]

## Paper

A full research paper with literature review, methodology, results, discussion, and references should be included in the repository as a PDF. That document provides the complete academic framing for the project and complements the code, figures, and model outputs presented here.[4][10]


Suggested file placement:

```text
paper/democratic_voter_shift_paper.pdf
```

You can also link it directly in the README once uploaded:

```markdown
[Read the full paper](paper/democratic_voter_shift_paper.pdf)
```

## Limitations

This project uses county-level analysis, so its conclusions are ecological rather than individual-level. The text-based extension is also constrained by geographic aggregation and source availability, which likely reduced its added explanatory value.[5][6]

## Tools

- Python
- pandas
- scikit-learn
- Plotly
- JupyterLab
- American Community Survey data
- Pennsylvania election returns

## Next Steps

- Upload the final paper PDF to `paper/`.
- Add `requirements.txt` and, if useful, an `environment.yml` file.
- Replace placeholder image filenames with your actual exported figure names.
- Pin the repository on your GitHub profile after the README and key outputs are in place.[7][14][8]
