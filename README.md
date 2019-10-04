# 2019 Toronto Health Hack (4-5 October 2019)

- https://www.tdothealthhack.com

## Documentation

- MIMIC-III Clinical Database: https://mimic.physionet.org/
- eICU Collaborative Research Database: https://eicu-crd.mit.edu/
- General Internal Medicine (GIM) dataset
- Medical Imaging in Cervical Spine Trauma (MICST) dataset

## Getting started

The datasets are hosted on Google Cloud, which requires a Gmail account to manage permissions.

1. Create a [Gmail account](https://www.google.com/gmail/about/), if you don't already have one. It will be used to manage your access to the resources.
2. Give your gmail address to the session hosts.

## Databases on BigQuery

BigQuery is a database system that makes it easy to explore data with Structured Query Language ("SQL").

1. [Open BigQuery](https://console.cloud.google.com/bigquery?project=tdothealthhack-team).
2. At the top of the console, select `tdothealthhack-team` as the project. This indicates the account used for billing.
3. "Pin" a project to the resources menu to view available datasets. In the Resources menu on the left, click "Add data", "Pin a project", then add the following project names: `physionet-data` and `tdothealthhack-data`.
4. You should be able preview the data available on these projects using the graphical interface.
5. Now try running a query. For example, try counting the number of rows in the demo eICU patient table:

   ```SQL
   SELECT count(*)
   FROM `physionet-data.eicu_crd_demo.patient` 
   ```

## Executable notebooks on Colab

Several tutorials are provided below. Requirements for these notebooks are: (1) you have a Gmail account and (2) your Gmail address has been added to the appropriate Google Group by the workshop hosts.

* [01-accessing-the-data.ipynb](https://colab.research.google.com/github/MIT-LCP/2019_toronto_health_hack/blob/master/tutorials/eicu/01-accessing-the-data.ipynb)
* [02-explore-patients.ipynb](https://colab.research.google.com/github/MIT-LCP/2019_toronto_health_hack/blob/master/tutorials/eicu/02-explore-patients.ipynb)
* [03-severity-of-illness.ipynb](https://colab.research.google.com/github/MIT-LCP/2019_toronto_health_hack/blob/master/tutorials/eicu/03-severity-of-illness.ipynb)
* [04-summary-statistics.ipynb](https://colab.research.google.com/github/MIT-LCP/2019_toronto_health_hack/blob/master/tutorials/eicu/04-summary-statistics.ipynb)
* [05-prediction.ipynb](https://colab.research.google.com/github/MIT-LCP/2019_toronto_health_hack/blob/master/tutorials/eicu/05-prediction.ipynb)
* [Understanding Electronic Health Records with BigQuery ML](https://github.com/GoogleCloudPlatform/healthcare/blob/master/datathon/mimic_eicu/tutorials/BigQuery_ML.ipynb)
* [Datathon Tutorial](https://github.com/GoogleCloudPlatform/healthcare/blob/master/datathon/mimic_eicu/tutorials/bigquery_tutorial.ipynb)
* [MIMIC-IV](https://colab.research.google.com/github/MIT-LCP/2019_toronto_health_hack/blob/master/tutorials/mimic-iii/summary-statistics.ipynb)

## R Markdown

Datasets can also be queried directly from R. You should be able to run the following RMarkdown notebook in a local version of RStudio: https://github.com/MIT-LCP/2019_toronto_health_hack/blob/master/tutorials/mimic-iii/mimic-iii-los.Rmd
