# 🤖 Alicia Mbithe Munyao | Data Science Portfolio

## About Me

Hello! I'm **Alicia Mbithe Munyao**, an aspiring Data Scientist pursuing a Bachelor of Science in Applied Statistics and Data Science while specializing in Data Science at Moringa School.

I enjoy extracting insights from complex datasets using statistics, programming, and predictive analytics to solve real-world problems.

---

## Technical Skills

### Programming

- Python
- SQL

### Data Science

- Data Cleaning
- Exploratory Data Analysis
- Feature Engineering
- Predictive Analytics
- Statistical Modeling

### Data Visualization

- Matplotlib
- Power BI
- Excel
- Tableau

### Statistics

- Probability
- Regression Analysis
- Hypothesis Testing
- Statistical Inference

---

# 📁 Projects

## 📈Evaluating Customer Behavior

### Objective

A retail company that operates stores in three distinct regions: City Center, Suburb, and Rural, I was tasked with analyzing customer behavior and preferences across these locations.
The goal is to help the company answer two key questions:

- Do customer spending patterns, satisfaction levels, and product preferences differ across store locations?
- Do promotional periods result in significantly higher spending compared to non-promotional periods?

### Dataset

This dataset was created for educational purposes to analyze customer behavior and preferences across three locations. It includes Store location, Amount Spent, Customer Satisfaction, Product Ctegory and Purchase type.

### Methodology

- Data Cleaning
- Exploratory Data Analysis
- Hypothesis Testing
- Interpretion and reporting
- Building Visualizations
- Modeling

### Results

- Spending across locations: Significant differences found all three location pairs differ, with gaps up to 95% well above the 15% business threshold.
- Satisfaction across locations: Significant differences found all three location pairs differ, clearing the 1.0-point threshold.
- Promotional vs. non-promotional spending: No significant difference . Mean difference was only $0.25 — far below the $15 threshold needed to justify promotional costs.
- Product category preference across locations: No significant association found. Category mix is consistent across all three locations

### Conclusion

- This analysis set out to answer two business questions for the retail company: whether spending, satisfaction, and product preferences differ across store locations, and whether promotions actually drive higher spending. Using assumption-driven test selection across four hypotheses Kruskal-Wallis for spending and satisfaction (both failed key parametric assumptions), Mann-Whitney U for promotional spending, and Chi-square for category preference the results split cleanly into two categories: real, actionable differences and null findings that are just as important.
- Location matters a lot. Spending differs significantly across every pairwise location comparison, with gaps as large as 95% between City Center and Rural, far exceeding the 15% business threshold. Satisfaction also differs significantly across all three locations, clearing the 1.0-point threshold. Together, these findings justify genuinely differentiated strategies inventory, staffing, and service investment tailored per location rather than a uniform, one-size-fits-all approach.
- Promotions and category mix do not. The promotional analysis found essentially no effect: a $0.25 average spending difference between promotional and non-promotional periods, nowhere near the $15 threshold needed to justify the margin cost of running promotions. Similarly, product category preference showed no meaningful association with location. These are arguably the most financially significant findings in the whole project they suggest the company may currently be spending money on promotions without a demonstrated return, and that customizing inventory mix by location isn't supported by the data.
The core limitation throughout is that this is observational data: without customer IDs, timestamps, or demographic information, it's not possible to fully rule out confounds different populations shopping at different locations, or seasonal timing effects on the promotional comparison. The recommendation isn't just "here's what the data says," but "here's what additional data would let the company say this with more confidence."
Bottom line for the business: differentiate by location (spending and service), but stop treating promotions and location-specific category stocking as effective levers until better-designed data or a controlled experiment says otherwise. The analysis also modeled good statistical practice throughout — checking assumptions before choosing tests, correcting for multiple comparisons, and judging results against pre-defined business thresholds rather than p-values alone — which is what surfaced the promotional non-effect as a genuine, trustworthy finding rather than an artifact of an underpowered or poorly chosen test.

---

## 📈 Forest Fires Prevention

### Objective

- As a junior data analyst my task was to support efforts to reduce the damage caused by wildfires by identifying patterns in past fire occurrences and predicting areas at high risk. 
- Wildfires are highly unpredictable and are influenced by a combination of environmental conditions, weather patterns, and geographic factors. The company relies on data-driven insights to allocate firefighting resources efficiently and implement preventive measures before fires escalate.
- The company's goals;
-Analyze the factors that contribute to fire size and severity.
-Develop models capable of predicting high-risk areas.
-Provide actionable recommendations to aid in risk mitigation

### Dataset

- This dataset was created for educational purposes to identify patterns in past fire occurrences and predict areas at high risk. . It includes variables(x and y), month, day, FFMC,	DMC,	DC,	ISI,	temp,	RH,	wind,	rain and area.

### Methodology
- Load dataset
- Exploratory Data Analysis
- Regression models
- Evaluating model diagnostics
- Regularization
- Binary classification
- Logistic regression models

### Results
-Regression: Weather/spatial predictors showed almost no relationship with burned area (|r| ≤ 0.07). Baseline model R² ≈ 0.01; a more complex model (interactions, quadratic terms, month indicators) only reached R² ≈ 0.07, with adjusted R² ≈ 0.03 and worse BIC added complexity wasn't justified.
-Diagnostics: Residuals were non-normal and heavy-tailed (driven by the large number of zero-area fires); a handful of large fires were flagged as influential via Cook's Distance.
-Regularization: Ridge and Lasso performed nearly identically (MSE ≈ 1.95, log scale). Lasso zeroed out all but ~2 coefficients, confirming most predictors added no real value.
-Classification: Logistic regression predicting "large vs. small" fire (median split) achieved only ~48% accuracy at or below the ~50% baseline of guessing the majority class. The model could not meaningfully distinguish large fires from small ones.
-Multicollinearity: Ruled out all VIF values were low . The weak performance wasn't due to redundant predictors.

Bottom line: None of the models: regression, regularized, or classification found meaningful predictive signal in this dataset's weather and spatial features. This matches confirmed it's a genuinely difficult prediction problem rather than a modeling failure.

### Conclusion
- The available weather and spatial variables in the Forest Fires dataset simply don't contain enough signal to reliably predict either the size of a fire (regression) or whether a fire will be larger than average (classification). This wasn't due to a modeling mistake, multicollinearity, or a fixable technical issue VIF was low, several modeling approaches were tried (baseline, interactions, quadratic terms, regularization), and all converged on the same weak result.

- The practical takeaway isn't "the analysis failed" — it's that the current features aren't the right ones for this prediction task. The recommendation is to shift focus from tuning models further to collecting better data: fuel load/vegetation density, ignition source, terrain/elevation, and finer-grained weather readings would likely carry far more information about fire size than temperature, humidity, wind, and rain alone. In the meantime, the existing fire-weather danger indices (FFMC, DMC, DC, ISI) are better suited to flagging ignition risk than to predicting how large a fire will grow so resource allocation decisions should lean on those indices for that purpose rather than expecting precise burn-size forecasts from this dataset.

---

## Contact

📧 Email:aliciamunyao25@gmail.com

💼 LinkedIn:https://www.linkedin.com/in/alicia-munyao-3abb27369

🌐 Portfolio:https://github.com/aliciamunyao25-jpg/Data-Science-portfolio.git
