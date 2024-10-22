# Skincare Product Optimization for Boxing Day Sales
## 1. Project Overview

The project focuses on using **Zero-One Integer Programming** to optimize the selection of skincare products for an upcoming **Boxing Day Sale**. The goal is to maximize revenue while catering to customer needs based on skin types and budget constraints.

### Key Objectives:
- **Optimize skincare product mix**: Select the best combination of skincare products tailored to different skin types and budget categories.
- **Maximize revenue**: Use integer programming to determine the optimal selection of products to maximize sales revenue.
- **Handle real-world constraints**: Include constraints such as non-repeating products across different price categories and skin types.
  
## 2. Files in this Repository

- `Decision_Making.ipynb`: Jupyter notebook containing the Python code used to build and solve the integer programming model using Gurobi.
- `Decision Making_report.pdf`: The individual report explaining the problem formulation, model, results, and recommendations based on the analysis.
- `Skincare_Product_Data.xlsx`: The dataset of skincare products used for the analysis, including product types and prices. The entire dataset is from Kaggle website: [Skincare Recommendation Engine](https://www.kaggle.com/code/eward96/skincare-recommendation-engine/notebook).


## 3. Instructions for Running the Code

To run the notebook (`Decision_Making.ipynb`), ensure you have the following installed:
- **Python 3.13.0**
- Libraries: `pandas`, `gurobipy`, `numpy`

### Steps:
1. Install the necessary libraries using:
   ```bash
   pip install pandas gurobipy numpy
   ```
2. Open the Jupyter notebook in your environment and run the cells sequentially to replicate the analysis and optimization results.
3. The notebook includes:
   - Data preprocessing: Cleaning and structuring the skincare product data.
   - Model building: Formulating the objective function and constraints.
   - Optimization: Solving the Zero-One Integer Programming model using Gurobi to find the optimal product mix.

### Expected Outputs:
- **Optimal Product Mix**: A set of skincare products for each skin type (oily, combination, normal/dry) across three budget categories (£30, £50, £100).
- **Optimal Revenue**: The model will output the maximum possible revenue based on the selected product mix.

## 4. Analysis Overview

### 4.1 Problem Definition
- The challenge is to curate an optimal selection of skincare products for **LOOKFANTASTIC's** Boxing Day sale to maximize revenue, while considering customer preferences for skin type (oily, combination, normal/dry) and budget constraints (under £30, under £50, under £100).

### 4.2 Data Collection
- The skincare product data was sourced from a **Kaggle** dataset and cleaned to include only facial skincare products.
- The expected customer numbers were estimated based on **SimilarWeb** data for website traffic and **Barclays Bank** reports on Boxing Day spending.

### 4.3 Decision Model
- **Zero-One Integer Programming** was used to formulate the problem. The decision variables represent whether a product is included in the optimal mix (1) or not (0).
- **Objective function**: Maximize total revenue from the selected product mix.
- **Constraints**: No product repetition across price categories, brand diversity within sets, and skin type distribution across budget ranges.

### 4.4 Results
- The optimization produced nine distinct product sets (one for each combination of skin type and budget range).
- The model achieved a globally optimal solution with a total projected revenue of **£319,320**.

### 4.5 Recommendations and Improvements
- **Product diversification**: Expand the product selection to cater to more specific skin concerns like sensitive or acne-prone skin.
- **Seasonal adjustments**: Modify product selections based on seasonal skincare needs, such as hydration for winter or sun protection for summer.
- **Incorporating customer feedback**: Analyze customer reviews and feedback to further refine the product selection.

## 5. Conclusion

This project successfully demonstrates the application of Zero-One Integer Programming to optimize product selection for a high-revenue event like Boxing Day. The model balances the need for brand diversity, skin type preferences, and customer budget constraints to maximize revenue.

## 6. License

This project is for academic purposes only as part of the **Data Analytics for Strategic Decision Making** module.
