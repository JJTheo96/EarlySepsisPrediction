# Content

## `prepare_mimiciii.ipynb`
* process adult data from MIMIC-III;
* train-val-test split into folder `./data/data_mimiciii/`;
* generate `baseline_data` and `engineered_data` into folder `../datasets/MIMICIII/adults`.

## `prepare_Cinc2019.ipynb`
* process adult data from CinC 2019;
* train-val-test split into folder `./data/data_Cinc2019/`;
* generate `baseline_data` and `engineered_data` into folder `../datasets/Cinc2019`.

## `model_RF`, `model_LR`, `model_XGB`, `model_LSTM`
* `./model_**.ipynb` contains the code for model, including:
    * data processing;
    * feature selection;
    * hyper-parameter tuning;
    * training and validation process;
    * test process;
    * test on real neonatal dataset;
    * test on artificial neonatal dataset.
* `./trained_models/`
    * **BDWOFS** : using Baselien Data WithOut Feature Selection;
    * **BDWFS** : using Baselien Data With Feature Selection;
    * **EDWOFS** : using Engineered Data WithOut Feature Selection;
    * **EDWFS** : using Engineered Data With Feature Selection;
    * each floder contains 5 models from 5-fold cross validation.
* `./prediction/` and `./label/`
    * used only for the test process.
* `./figs/`
    * store figures, including feature importance, test results and others.

## `model_XGB_downsample`
* this is a variation of the XGB model using downsampled data instead of upsampling;
* the results are slightly than the one using upsampling;
* training process is much faster;

## `model_RF_AUG` and `data_AUG`
* A **trial** using augmented data instead of duplicated data for upsampling;
* achieves a similiar test performance.

## `data_figs`
*  stores generated figures for datasets, including age distirbution, featuer missing rate, sepsis label distribution ...
