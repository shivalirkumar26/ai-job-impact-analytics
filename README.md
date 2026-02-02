AI Job Impact Analytics

Will AI really take over our jobs — or just change them?

This project explores how artificial intelligence impacts jobs across regions, industries, and seniority levels, using advanced SQL modelling and analytics-first design.
Rather than speculating, it quantifies AI exposure, automation risk, and skill vulnerability using a structured data model and reproducible logic.

⸻

Project Objective

To answer three key questions:
	1.	Which jobs are most exposed to AI — and why?
	2.	Does high AI exposure always mean high automation risk?
	3.	How do region, job level, and skill composition influence AI impact?

The goal is not prediction hype, but decision-ready insights grounded in data.

⸻

Key Insights (Executive Summary)
	•	Most roles today fall under AI augmentation, not full automation
	•	Task composition and skill mix matter more than salary or seniority alone
	•	Roles with cognitive + low-resistance skills face the highest transformation pressure
	•	AI risk varies significantly across job families and regions, even within the same industry

⸻

Data Architecture & Modelling

This project was built SQL-first, with analytics logic pushed as close to the data layer as possible.

Schema Design
	•	Dimensions
	•	dim_job_role – job title, family, industry, level
	•	dim_skill – skill type and automation resistance
	•	dim_region – region, country, income group
	•	dim_job_ai_profile – AI exposure classification per role
	•	Facts
	•	fact_job_ai_exposure – AI exposure score, automation probability
	•	fact_job_salary – salary bands and averages
	•	bridge_job_skill – many-to-many job–skill mapping with importance weights

Why this design?
	•	Enables complex exposure scoring
	•	Supports region-specific analysis
	•	Scales cleanly for future projections

⸻

Analytics Logic (Highlights)
	•	AI Exposure Score
Weighted calculation based on:
	•	Skill importance
	•	Automation resistance (Low / Medium / High)
	•	AI Risk Categories
	•	Low Risk
	•	Medium Risk
	•	High Risk
	•	Skill-driven risk, not rule-based assumptions

All calculations are implemented in SQL views, not visualisation tools.

⸻

Views Used for Analysis

Key analytical views include:
	•	vw_job_ai_risk_summary
	•	vw_job_task_composition
	•	vw_region_ai_exposure
	•	vw_job_seniority_comparison
	•	vw_salary_vs_ai_exposure
	•	vw_ai_impact_distribution

These views form a single analytical layer, exported for visualisation.

⸻

Visualisation & Dashboard
	•	Built using Tableau Public
	•	Data sourced from SQL views (CSV exports)
	•	All visuals respond to global filters:
	•	Job Title
	•	Job Level
	•	Industry
	•	Region

Dashboard Design Principles
	•	Executive-first storytelling
	•	Minimal visual clutter
	•	Consistent colour semantics for risk levels
	•	Insight > decoration

⸻

Tools & Technologies
	•	PostgreSQL – data modelling & analytics
	•	Advanced SQL – views, aggregations, scoring logic
	•	Tableau Public – dashboard & storytelling
	•	GitHub – version control & documentation

(No paid tools or licenses used.)

⸻

Repository Structure

ai-job-impact-analytics/
│
├── sql/
│   ├── schema/
│   ├── dimensions/
│   ├── facts/
│   └── views/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── tableau/
│   └── dashboard/
│
└── README.md


⸻

Why This Project Matters

This project demonstrates:
	•	Real-world SQL modelling depth
	•	Ability to translate complex logic into business insight
	•	Strong end-to-end analytics thinking
	•	Portfolio-ready storytelling, not classroom exercises

It reflects how analytics is actually used in strategy, consulting, and data roles.

⸻

Possible Extensions
	•	Time-based AI impact projections
	•	Job transition pathways (reskilling scenarios)
	•	AI impact by education level
	•	Industry-specific deep dives

⸻

About Me

This project is part of my personal analytics portfolio, focused on:
	•	Business intelligence
	•	Data modeling
	•	Insight-driven storytelling

If you’re curious, feel free to explore the SQL, visuals, or reach out.


