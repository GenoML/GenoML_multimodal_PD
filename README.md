# Multi-Modality Machine Learning Predicting Parkinson’s Disease (Online Appendix)


## Summary
This is the online appendix for the manuscript titled *"Multi-Modality Machine Learning Predicting Parkinson’s Disease"*, where we integrated clinico-demographic, genetic, and transcriptomic data within an automated machine learning open science framework (GenoML) to predict Parkinson’s disease and identify potential novel therapeutic targets for drug development

## Workflow Diagram 
![Workflow Diagram](https://github.com/GenoML/GenoML_multimodal_PD/blob/main/plots/workflow_fig1_new.jpeg)

## Helpful Links 
- BioRxiv pre-print (coming soon!)
- [streamlit interactive app](https://urldefense.com/v3/__https://share.streamlit.io/anant-dadu/shapleypdpredictiongenetics/main__;!!DZ3fjg!o0svR5aS1O5sxyVNhbUpOZKFslC7o63prvIfypa7vLnCWaxLD3x3hz5q5MIAmXG7Qw$)
    - [streamlit interactive app repository](https://github.com/anant-dadu/shapleyPDPredictionGenetics)
- GenoML short paper (coming soon!)
    - [GenoML website](https://genoml.com/)
    - [GenoML repository](https://github.com/GenoML/genoml2)


## Orientation 
- The `scripts/` directory includes the pre-processing, munging, training, tuning, optmiziation, and networks scripts (coming soon!) 
- The `topmodel_G1E5T1E2/` directory includes the
    - Top model's figures, metrics, and .joblib model
    - Genetics at a p-value threshold of 1E-5 only figures, metrics, and .joblib model
    - Transcriptomics at a p-value threshold of 1E-2 only figures, metrics, and .joblib model
    - Clinicodemographic only figures, metrics, and .joblib model
- The `shapAnalysis/` directory includes the 
    - Surrogate XGBoostClassifier models for the combined model, rsIDs only, ENSGs only, or rsIDs and ENSGs only
    - Figures showing top 5% of features in the combined model 
    - A directory with dependence plots between each SNP and its effect on PRS90 
- The `trained_joblibs/` directory includes all the 49 trained models in `.joblib` format
- The `tuned_joblibs/` directory includes all the 49 tuned models in `.joblib` format
- The `trained_metricsplots/` includes all metrics for the 49 trained models 
    - `*.trainedModel_withheldSample_probabilities.png`
    - `*.trainedModel_withheldSample_ROC.png`
    - `*.training_withheldSamples_performanceMetrics.csv`
- The `tuned_metricsplots/` directory includes all metrics for the 49 tuned models 
    - `*.tunedModel_CV_Summary.csv`
    - `*.tunedModel_top10Iterations_Summary.csv`
- The `tested_metricsplots/` directory includes all metrics for the 49 tested models in PDBP
    - `*.testedModel_allSample_probabilities.png`
    - `*.testedModel_allSample_ROC.png`
    - `*.testedModel_allSamples_performanceMetrics.csv`
