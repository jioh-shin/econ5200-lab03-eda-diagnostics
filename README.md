Pipeline Health Check — EDA, Corruption & Distribution Shift
Objective

Analyze and improve the reliability of an economic data pipeline by identifying data-quality issues through exploratory data analysis (EDA) and monitoring distribution shifts between training and inference data.

Methodology
Identified and corrected five planted data-quality issues using EDA, including negative GDP values, life expectancy stored in months, duplicate observations, inconsistent percentage units, and a GDP unit mismatch.
Measured distribution shift between training and inference data using the Population Stability Index (PSI).
Compared manual EDA with automated profiling using ydata-profiling.
Created a reusable eda_utils.py module for impossible-value checks, PSI calculation, and EDA summaries.
Built an interactive pipeline-health dashboard to inspect distributions, PSI results, data-quality constraints, and cleaned versus corrupted data.
Key Findings

Five data-quality issues were identified and corrected through manual EDA. The GDP distribution showed a significant shift between training and inference data, with a PSI of 2.2899. Manual EDA also identified domain-specific problems that automated profiling alone could not fully detect, showing the importance of combining automated tools with domain-based validation.
