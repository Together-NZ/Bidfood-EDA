Bidfood EDA 

**Overview**

Bidfood EDA is a lightweight exploratory data analysis (EDA) pipeline for Bidfood NZ customer and sales data. It unifies customer identities, cleans and joins raw tables, computes KPIs, and generates visual diagnostics (Pareto, distributions, time-between purchases, repertoire by Class\_Code, branch/industry summaries, and gap analysis).
For full logic explanations, gotchas, and a runbook, see the Word document for details.

**What it does**

	  • Loads core tables (branch, customer, product, sales) from BigQuery and applies cleaning rules.
	  • Builds a unified customer identity (unified\_customer\_key) via staged de-duplication.
	  • Joins customers ↔ sales and runs data-quality checks.
	  • Computes yearly KPIs (revenue, orders, AOV, unique customers) and Pareto/value distributions.
	  • Calculates inter-purchase intervals (binned) with cumulative insights.
	  • Produces industry and branch summaries; includes a cafés/coffee shops vertical view.
	  • Repertoire analysis by Class\_Code with a frequency matrix to support cross-sell.
	  • Optional “gaps” logic (e.g., exclude national accounts, non-purchased categories).


**Getting started**

1. Python: 3.10–3.12 recommended.
2. Install dependencies:
   pandas, numpy, matplotlib, seaborn, google-cloud-bigquery, pyarrow, db-dtypes
   (Example: pip install pandas numpy matplotlib seaborn google-cloud-bigquery pyarrow db-dtypes)
3. Authenticate to GCP:
   gcloud auth application-default login
   (or set GOOGLE\_APPLICATION\_CREDENTIALS to a service-account JSON)


Support

• See the Bidfood-EDA_Handover_Documentation.docx for the detailed handover guide, troubleshooting, and future-enhancement ideas.


