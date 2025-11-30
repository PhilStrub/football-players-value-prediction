# A Soft-Routing Pipeline to Predict Football Players' Market Value

**Course:** Econometrics Coursework  
**Authors:** Lorenzo Caputi, Paride Lauretti, Andrea Pettenon, Andrea Procopio, Filippo Strub  

## Overview

This project tackles the prediction of professional football players’ **market value** using demographic, contractual, and performance-related data.  
Due to strong nonlinearities and multimodal feature distributions, we implement a **soft-routing pipeline** combining a binary classifier and two regressors (base and top-valued).  
The final prediction is a weighted average of the two regressors, improving both accuracy and stability across folds.

---

## Usage

In order for the scripts to work correctly, run the notebooks in the following order:

1. `preprocessing.ipynb`  
2. `model_selection.ipynb`  
3. `error_analysis.ipynb`  
4. `autoencoders.ipynb`  
5. `generate_predictions.ipynb`

> Make sure to verify where the **preprocessed datasets** are saved before running subsequent scripts.

---

## Key Notes

- The dataset is split into training and test sets containing demographic, performance, and contract data.  
- The **soft-routing approach** uses:
  - A **classifier** to detect top 5% high-value players,  
  - A **base regressor** for the general population, and  
  - A **top regressor** specialized for top-valued players.  
- The combination yields improved predictive performance (CV RMSE ≈ **609k EUR**) compared to standard tree-based models.
