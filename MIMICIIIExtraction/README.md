# Content
## `adults_by_Bigquery.ipynb`
* Extract adult data from MIMIC-III using Bigquery;
* Must be used in **Google Colab**.

## `neonates_by_Bigquery.ipynb`
* Extract neonatal data from MIMIC-III using Bigquery;
* Must be used in **Google Colab**.

## `MIMIC_IV_by_Bigquery.ipynb`
* Extract **only adult** data from MIMIC-IV using Bigquery;
* Must be used in **Google Colab**.

## `post_process.ipynb`
* used after data extraction:
    * For sepsis positive:
		1. discard patients whose los < 6 hrs;
		2. discard patients who have no recording with the 6 hrs ahead the sepsis onset time;
		3. integrate all the events in one-hour-interval into hourly data point, e.g. all rows within the time range 17:00-18:00 will be intergrated into one row at 17:00.
	* For sepsis negative:
		1. discard patients whose los < 6 hrs;
		2. when los is larger than 100 hrs, only crop out the first 100 hr data;
		3. intergrate data into hourly format as above.
* input: `original_sepsis/` and `original_non_sepsis/`;
* output: `processed_sepsis/` and `processed_non_sepsis/`;

## `./NonSQL/`
* Extraction strategy using `Pandas` and `Dask`