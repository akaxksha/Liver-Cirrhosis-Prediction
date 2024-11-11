Here's an improved README file:

# Liver Cirrhosis Prediction

Liver cirrhosis is a serious health condition, particularly common in North America, and often associated with prolonged alcohol consumption. This project aims to predict the stage of liver cirrhosis in patients based on lifestyle factors and various health indicators.

## Objective

Liver cirrhosis progression can be classified into four stages:

1. **Stage 1**: Normal
2. **Stage 2**: Fatty Liver
3. **Stage 3**: Liver Fibrosis
4. **Stage 4**: Liver Cirrhosis

The goal of this project is to develop a predictive model to determine the liver disease stage of a patient based on a variety of clinical and demographic features, which include both numerical and categorical data.

## Project Context

Cirrhosis represents an advanced stage of liver fibrosis caused by liver diseases such as hepatitis and chronic alcoholism. The dataset used in this project was collected during a Mayo Clinic study on primary biliary cirrhosis (PBC) between 1974 and 1984. It includes information on 424 patients, with 312 participants in a randomized trial for the drug D-penicillamine and an additional 112 non-trial patients monitored for survival. This data was gathered to examine liver disease progression and survival rates.

This project draws from:

- *Counting Processes and Survival Analysis* by Fleming and Harrington (1991)
- Studies published in *Hepatology* and *New England Journal of Medicine* on PBC

## Dataset Description

The dataset consists of the following features:

| **Feature**      | **Description**                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID               | Unique identifier for each patient                                                                                                                        |
| N_Days           | Days between registration and the earlier of death, transplantation, or study end date in July 1986                                                      |
| Status           | Patient status: C (censored), CL (censored due to liver transplant), or D (death)                                                                        |
| Drug             | Drug type administered: D-penicillamine or Placebo                                                                                                        |
| Age              | Age (in days)                                                                                                                                            |
| Sex              | Gender: M (Male) or F (Female)                                                                                                                           |
| Ascites          | Presence of Ascites: N (No) or Y (Yes)                                                                                                                   |
| Hepatomegaly     | Presence of Hepatomegaly: N (No) or Y (Yes)                                                                                                              |
| Spiders          | Presence of Spiders: N (No) or Y (Yes)                                                                                                                   |
| Edema            | Presence of Edema: N (no edema and no diuretic therapy), S (edema without diuretics, or resolved by diuretics), Y (edema despite diuretic therapy)       |
| Bilirubin        | Serum Bilirubin (in mg/dl)                                                                                                                               |
| Cholesterol      | Serum Cholesterol (in mg/dl)                                                                                                                             |
| Albumin          | Albumin (in gm/dl)                                                                                                                                       |
| Copper           | Urine Copper (in µg/day)                                                                                                                                 |
| Alk_Phos         | Alkaline Phosphatase (in U/liter)                                                                                                                        |
| SGOT             | Serum Glutamic Oxaloacetic Transaminase (SGOT) (in U/ml)                                                                                                 |
| Triglycerides    | Triglycerides (in mg/dl)                                                                                                                                |
| Platelets        | Platelet count per cubic ml (1000/ml)                                                                                                                    |
| Prothrombin      | Prothrombin time (in seconds)                                                                                                                            |
| Stage            | Histologic stage of the disease (1-4)                                                                                                                    |

## Acknowledgements

This dataset is available in Appendix D of:

**Fleming, T.R., & Harrington, D.P. (1991). Counting Processes and Survival Analysis.** *Wiley Series in Probability and Mathematical Statistics*, John Wiley and Sons Inc., New York. 

This project aims to build upon these foundational studies to provide a reliable tool for predicting cirrhosis progression stages.


## Steps to Run

```
  1. conda deactivate
  2. conda activate clg_project
  3. export FLASK_DEBUG=1
  4. flask run
  5. open url in browser
```

## Reference Values by Disease Stage

| **Feature**         | **Normal**                      | **Fatty Liver**                   | **Fibrosis**                      | **Cirrhosis**                               |
|---------------------|---------------------------------|-----------------------------------|-----------------------------------|---------------------------------------------|
| **Ascites**         | No                              | No                                | No                                | Yes (common in advanced cirrhosis)         |
| **Hepatomegaly**    | No                              | Often Yes                         | Can be Yes                        | Usually Yes                                |
| **Spiders**         | No                              | No                                | No or occasionally Yes            | Yes (common in cirrhosis)                  |
| **Edema**           | No edema, no diuretic therapy   | Usually no edema, no diuretic     | May have no edema, no diuretic    | Edema present without diuretics, or persistent despite therapy |
| **Bilirubin (mg/dL)** | 0.3 - 1.2                    | 0.3 - 1.5                         | 0.3 - 2.0                         | 2.0 - 7.3 (higher levels indicate severe damage) |
| **Cholesterol (mg/dL)** | 160 - 200                  | 200 - 240                         | 160 - 250                         | 160 - 300 (may be lower in severe cases)    |
| **Albumin (g/dL)**  | 3.5 - 5.0                       | 3.5 - 4.5                         | 3.0 - 4.5                         | 2.0 - 3.5 (reduced in cirrhosis)            |
| **Copper (mcg/dL)** | 80 - 120                        | 80 - 150                          | 80 - 175                          | 100 - 175 (may increase in cirrhosis)       |
| **Alkaline Phosphatase (U/L)** | 44 - 147           | 100 - 200                         | 100 - 300                         | 300 - 1500 (significantly elevated)         |
| **SGOT (AST) (U/L)** | 10 - 40                       | 30 - 100                          | 30 - 150                          | 100 - 200 (higher values indicate damage)   |
| **Triglycerides (mg/dL)** | 45 - 150                | 150 - 200                         | 100 - 200                         | 100 - 150 (may decrease in cirrhosis)       |
| **Platelets (x10^9/L)** | 150 - 400                 | 150 - 350                         | 100 - 300                         | 62 - 200 (often reduced in cirrhosis)       |
| **Prothrombin Time (seconds)** | 9 - 12.5           | 10 - 13                           | 10 - 13                           | 12 - 15 (may increase due to impaired function) | 

This table organizes the typical values and symptoms by stage to aid in assessing and predicting liver cirrhosis progression.


