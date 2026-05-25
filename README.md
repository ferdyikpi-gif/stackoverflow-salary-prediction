# Tech Career Compensation Tracker: Stack Overflow Data Analysis

## Project Motivation
What professional choices actually move the needle when it comes to compensation in the tech industry? This project applies the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** framework to investigate the **2023 Stack Overflow Developer Survey** dataset. By examining data from over 44,000 tech professionals globally, this analysis answers critical real-world questions regarding high-paying developer roles, the economic impacts of remote work flexibility, and the primary human capital drivers behind tech salaries. 

## Key Business Questions Answered
1. **Question 1 (Descriptive):** Which developer roles command the highest median yearly compensation globally?
2. **Question 2 (Inferential):** Does an individual's chosen remote work status (Remote, In-person, Hybrid) significantly impact their total yearly compensation?
3. **Question 3 (Predictive):** What are the most critical features driving predicted salary outcomes in a Machine Learning model, and how accurately can we estimate salary based on them?

## Core Libraries Used
Pandas: Used for structural data manipulation, column cleaning, parsing qualitative experience string text, and data profiling.
* **NumPy**: Used for efficient vector-based operations.
* **Matplotlib & Seaborn**: Used to create clear, scannable, and publication-ready statistical data visualizations.
* **Scikit-Learn**: Used for data preprocessing (One-Hot Encoding), pipeline evaluation, data splitting (`train_test_split`), and training the `RandomForestRegressor` predictive engine.
* **Joblib**: Used for model serialization and disk-based file persistence.

## File Architecture
* `Supervised Learning.ipynb`: The primary executable Jupyter Notebook containing the full end-to-end data science process (gathering, data cleaning, exploratory visualizations, machine learning modeling, and creative deployment scenarios). Follows clean PEP8 coding structures and modular function blocks.
* `survey_results_public.csv`: The local cached dataset containing the public raw survey responses downloaded from the Stack Exchange repository.
* `developer_salary_pipeline.pkl`: The compiled, serialized machine learning pipeline file containing the trained model weights and one-hot encoding feature schema.
* `README.md`: This file, providing an administrative project blueprint, architectural manifest, and executive summary of results.

## Summary of Empirical Findings
* **The Domain Premium:** Traditional software engineering roles are being outpaced by cloud scalability and system architecture positions. **Cloud Infrastructure Engineers**, **DevOps Specialists**, and **Site Reliability Engineers (SREs)** lead global median compensation tables.
* **The Remote Advantage:** Choosing flexibility pays off. Completely **Remote** and **Hybrid** professionals consistently command higher median salaries than their strictly **In-Person** colleagues. Remote setups effectively unlock a borderless global job market, removing regional salary ceilings.
* **The Ultimate Ruler:** Machine learning feature importance configurations show that **Years of Professional Coding Experience (`YearsCodePro`)** is the single most dominant predictive driver of tech salaries, far outweighing formal education types or specific role variations.
* **Model Evaluation Metrics:** The baseline `RandomForestRegressor` model achieved an **$R^2$ Score of 0.1147** with a **Mean Absolute Error (MAE) of $45,335.94**. This indicates that while broad roles, flexibility, and years of experience account for roughly 11.5% of total salary variance globally, the rest is influenced by factors like company size, specific geographic location, or negotiation.

## Acknowledgments
* Data provided openly and generously via the public survey archiving systems maintained by **Stack Overflow**.