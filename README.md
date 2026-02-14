# Rachel-W.-Econ-580-Replication
# Econ 580 Replication: Wu (2018)
### Gendered Language on the Economics Job Market Rumors Forum

This repository contains my replication of key results from:

Wu, A. (2018). *Gendered Language on the Economics Job Market Rumors Forum*. AEA Papers and Proceedings, 110, 175–179.

The goal of this project is to replicate table 1, Table 2, and Figure 1 using the replication data provided by the author, and to compare OLS and LASSO estimation results as discussed in the paper by reestimating Table 1 using an OLS predictive model. 

---

## Repository Structure

- `FullLasso.py`  
  Implements LASSO estimation and prediction following Wu’s specification.

- `OLSExample.py`  
  Implements OLS regression for comparison to the LASSO results.

- `TablesAndFigures.py`  
  Generates replication tables and figures.

- `vocab10K.csv`  
  Word-level marginal effect data.

- `trend_stats.csv`  
  Time-series trend data used for figure replication.

---

## Data

All data used in this project comes from the official replication materials associated with Wu (2020). No additional data cleaning beyond what is required to load the provided files was performed.
## Note on Data Access

Due to GitHub file size limits, the full dataset "gendered_posts.csv" and “X_word_count.npz”
is not included in this repository.

Please download the official replication data from the original Wu (2018)
replication package and place the files in the project root directory
before running the scripts.

## All Data used (solely "vocab10k.csv", "keys_to_X.csv", and "trends_stas.csv" included in this package per note above)	
1. “gendered_posts.csv”:	
- a	dataset	of	Female/Male	posts	identified	from	the	four-year	sample	of	EJMR	
data.	
2. “vocab10K.csv”:	
- a	list	of	the	most	frequent	10,000	words	that	emerge	from	2.2	million	posts	from	
Oct	2013	to	Oct	2017,	and	each’s	marginal	probability	on	a	post	discussing	a	
female	from	the	Lasso	models.	
3. “X_word_count.npz”
- this	file	contains	a	matrix	that	records	the	number	of	occurrences	of	each	word	
from	the	most	frequent	10,000	words	in	each	post.	This	matrix	is	called	in	the	
python	programs	for	logistic/linear	Lasso	models.	
4. “keys_to_X.csv”
- this	file	contains	unique	identifiers	for	each	post	in	each	thread	(title_id	and	
post_id)	in	the	Same order	as	the	matrix of	word	counts	saved	in	the	.npz	
format. Useful	for	merging in	the	python	programs	below.	
5. “trend_stats.csv”
- monthly	summary	stats	for	Figure	1

## Requirements

This project was implemented in Python.

Required packages:
- pandas
- numpy
- scikit-learn
- statsmodels
- matplotlib

Install via:

```bash
pip install pandas numpy scikit-learn statsmodels matplotlib


## Files Included
- FullLasso.py – replication of LASSO results
- OLSExample.py – OLS comparison results
- TablesAndFigures.py – table and figure generation


## Instructions to Run
1. Install required packages:
   - pandas
   - numpy
   - sklearn
2. Run scripts in this order:
   - OLSExample.py
   - FullLasso.py
   - TablesAndFigures.py

## Author
Rachel Williams  
University of Wisconsin–Madison
