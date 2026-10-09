# Job Market Skills Demand Analysis

## Project Overview

This project explores job-market data to understand the skills, roles, locations, experience requirements, work arrangements, and disclosed salary ranges represented in the dataset.

The analysis is performed in Python using **Pandas, NumPy, Matplotlib, and Seaborn**, with Google Colab as the development environment.

## Objectives

- Identify the most frequently listed job roles.
- Measure the frequency of skills mentioned in job postings.
- Compare skill mentions across job-role categories.
- Explore job-posting locations and work modes.
- Examine postings marked as fresher-friendly.
- Compare disclosed salary ranges across roles.
- Produce charts and summary tables to communicate findings.

## Tools and Technologies

- Python
- Google Colab / Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Dataset

The project uses an Indian tech job-market dataset containing **23,201 records and 32 columns**.

Fields used in the analysis include:

- `job_title`, `company_name`, `role_category`
- `primary_city`, `location`, `work_mode`
- `skills_required`, `skills_count`, `skill_domain`
- `experience_raw`, `experience_min_yrs`, `experience_max_yrs`
- `salary_disclosed`, `salary_min_lpa`, `salary_max_lpa`, `salary_midpoint_lpa`
- `is_fresher_friendly`

**Dataset source:** [India Tech Job Market — 23K Records on Kaggle](https://www.kaggle.com/datasets/shree0910/india-tech-job-market-2026-23k-records)

Check the dataset's license and terms before redistributing the dataset or derived records. If redistribution is not permitted, publish the notebook and analysis outputs only where allowed, and provide the source link instead of uploading the raw or cleaned data.

## Project Workflow

1. **Load the data** using Pandas.
2. **Inspect the dataset** for dimensions, column names, data types, missing values, and duplicates.
3. **Prepare the data** by standardizing text and checking numeric fields.
4. **Analyze job roles** using frequency counts and percentages.
5. **Analyze skill demand** by extracting skill labels and counting postings that mention them.
6. **Compare skills by role** using counts and percentage-based heatmaps.
7. **Explore locations and work modes** using bar charts.
8. **Analyze fresher-friendly postings** using the dataset's `is_fresher_friendly` flag.
9. **Analyze disclosed salaries** after excluding undisclosed or invalid salary values.
10. **Export charts, summary tables, and findings** for reporting.

## Findings Observed During Analysis

The following figures were observed in the notebook outputs during the project. They describe this dataset only and are not a census of the entire Indian job market.

- **Total job postings:** 23,201.
- **Salary disclosure:** 2,768 postings were initially marked as salary-disclosed. A subsequent salary analysis retained 2,705 records with positive minimum salary values and valid salary ranges.
- **Fresher-friendly postings:** 4,182 postings were marked as fresher-friendly (**18.03%** of all records).
- **Most represented cities:** Mumbai (3,276 postings), Bangalore (2,830), Chennai (2,666), Pune (2,606), and Noida (2,585).
- **Work mode:** 18,701 postings were marked on-site, 2,347 hybrid, and 2,153 remote.
- **Fresher-friendly role counts:** Data Analyst (1,287), Data Scientist (880), Business Analyst (804), Machine Learning Engineer (794), Python Developer (219), and Data Engineer (198).
> **Salary figures:** Check the final executed notebook and `salary_by_role.csv` before adding role-wise salary claims. Earlier outputs may differ depending on which records were filtered.

## Visualizations

The notebook generates visualizations such as:

- Top job roles
- Most frequently mentioned skills
- Skill demand across roles
- Job postings by city
- Fresher-friendly postings by role
- Work-mode distribution
- Salary distribution and salary comparison by role, when usable salary data is available

Charts should be saved in the `visualizations/` directory before publishing. Update this README if your final notebook uses different filenames.

## Suggested Repository Structure

```text
job-market-skills-demand-analysis/
├── Job_Market_Skills_Demand_Analysis.ipynb
├── README.md
├── visualizations/
│   ├── top_15_skills.png
│   ├── cleaned_skills_by_job_role.png
│   ├── top_15_job_cities.png
│   ├── fresher_friendly_jobs.png
│   └── job_work_mode_analysis.png
└── results/
    ├── skill_demand.csv
    ├── role_skill_counts.csv
    ├── fresher_role_counts.csv
    ├── city_counts.csv
    ├── work_mode_counts.csv
    └── salary_by_role.csv
```

The folder and filenames above are a suggested structure. Upload only files that you have actually generated, and make sure the paths match your repository.

## How to Run

1. Download or open the notebook in Google Colab.
2. Download the dataset from the source linked above.
3. Upload the CSV when prompted, or update the file path in the notebook.
4. Run the notebook cells in order.
5. Review the charts, outputs, and exported tables.

## Limitations

- The dataset is a snapshot and may not represent currently open vacancies.
- Results depend on the coverage, quality, and collection method of the source dataset.
- Skill counts depend on how skill text is formatted and normalized. Similar labels and abbreviations may be counted separately unless explicitly standardized.
- The `is_fresher_friendly` field is a dataset-provided flag; it does not independently verify that a role accepts all fresh graduates.
- Salary figures are available for only a subset of postings. Salary ranges and units should be checked against the source before interpretation.
- A job-posting count is not the same as the number of unique employers or currently active vacancies.

## Future Improvements

- Improve skill normalization with a documented alias dictionary.
- Validate and standardize job titles, locations, and experience levels.
- Compare skill percentages within each role, not just raw counts.
- Add posting-date analysis if the date field is reliable.
- Validate salary units and compare salaries only for disclosed, valid records.
- Add a reproducible data dictionary and source/license notes.

## Author

**Anvitha Jain**

## License

Add a license for your own code if you want to specify reuse terms. The dataset may have a separate license; follow its terms and attribution requirements.
