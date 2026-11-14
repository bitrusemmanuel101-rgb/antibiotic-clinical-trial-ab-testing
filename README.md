# Gepotidacin vs Nitrofurantoin A/B Test Analysis  
### EAGLE-2 & EAGLE-3 Phase 3 Trials

*Last updated: November 2026*

---

## Summary

This project analyses the results of two phase 3 randomised controlled trials (EAGLE-2 and EAGLE-3) that compared a new antibiotic, **gepotidacin**, with the current standard treatment, **nitrofurantoin**, in women with uncomplicated urinary tract infections (UTIs).

Using two-proportion tests and confidence intervals, the analysis shows that gepotidacin was non-inferior to nitrofurantoin in both trials and superior in EAGLE-3.

---

## Background

Uncomplicated urinary tract infections are very common, and *E. coli* is the most frequent cause. Rising antimicrobial resistance has increased the need for new oral antibiotics. Gepotidacin is a first-in-class antibiotic that was tested against nitrofurantoin in two large phase 3 trials.

This project connects to my previous work on *E. coli* resistance to third-generation cephalosporins, which highlighted the growing resistance problem that new antibiotics like gepotidacin aim to address.

---

## Research Questions

1. Is there a statistically significant difference in therapeutic success rates between gepotidacin and nitrofurantoin?
2. Can gepotidacin be considered non-inferior to nitrofurantoin (using a 10% non-inferiority margin)?
3. How do the results of EAGLE-2 and EAGLE-3 compare?

---

## Dataset

Data were extracted from the published results of the EAGLE-2 (NCT04020341) and EAGLE-3 (NCT04187144) trials.

| Trial    | Treatment       | Successes | Total | Success Rate |
|----------|-----------------|-----------|-------|--------------|
| EAGLE-2  | Gepotidacin     | 162       | 320   | 50.6%        |
| EAGLE-2  | Nitrofurantoin  | 135       | 287   | 47.0%        |
| EAGLE-3  | Gepotidacin     | 162       | 277   | 58.5%        |
| EAGLE-3  | Nitrofurantoin  | 115       | 264   | 43.6%        |

**Note:** These figures come from the primary analysis population (microbiological ITT, nitrofurantoin-susceptible) at the time of the interim analysis.

---

## Methodology

- Calculated success rates (proportions) for each treatment arm  
- Computed the difference in proportions  
- Performed two-proportion z-tests  
- Calculated 95% confidence intervals for the differences  
- Assessed non-inferiority using a pre-specified 10% margin  
- Compared unadjusted results with the adjusted results published in the paper  

---

## Key Results

| Trial    | Difference (Gep – Nitro) | 95% CI            | Non-inferior? | Superior? |
|----------|---------------------------|-------------------|---------------|---------|
| EAGLE-2  | +3.6% (unadjusted)        | Approx. –4% to 12% | Yes           | No      |
| EAGLE-3  | +14.9% (unadjusted)       | Approx. +7% to 23% | Yes           | Yes     |

Published adjusted differences:  
- EAGLE-2: +4.3% (95% CI –3.6% to 12.1%)  
- EAGLE-3: +14.6% (95% CI 6.4% to 22.8%)

---

## Important Context

- Both trials were **stopped early for efficacy** after a pre-planned interim analysis.  
- The published results are **adjusted** for baseline characteristics, while the calculations in this repository are **unadjusted**.  
- Early stopping can lead to slightly overestimated treatment effects.

---

## Conclusion

Gepotidacin demonstrated non-inferiority to nitrofurantoin in both EAGLE-2 and EAGLE-3, and superiority in EAGLE-3. These results support gepotidacin as a potential new oral treatment option for uncomplicated UTIs, particularly in the context of rising antimicrobial resistance.

---

## Limitations

- Analysis is based on summary counts rather than patient-level data  
- Used unadjusted estimates (published results are adjusted)  
- Both trials were stopped early, which can inflate the observed effect size  
- Results apply only to women with uncomplicated UTIs

---

## Tools Used

- Python (pandas, NumPy, SciPy, statsmodels)  
- Jupyter Notebook  
- Git & GitHub

---

## How to Run

1. Clone this repository  
2. Install the required packages: `pip install -r requirements.txt`  
3. Open the notebook and run all cells

---

## Data Sources

- Lancet paper: Wagenlehner et al. (2024). Oral gepotidacin versus nitrofurantoin...  
- ClinicalTrials.gov: [NCT04020341](https://clinicaltrials.gov/study/NCT04020341) (EAGLE-2)  
- ClinicalTrials.gov: [NCT04187144](https://clinicaltrials.gov/study/NCT04187144) (EAGLE-3)

---

*Author: Emmanuel Bitrus*
