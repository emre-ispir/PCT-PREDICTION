PCT-PREDICTION


Overview
This repository contains the complete machine learning pipeline developed for predicting elevated procalcitonin (PCT ≥ 0.5 ng/mL) from routine complete blood count (CBC) and inflammatory markers. The pipeline supports antimicrobial stewardship programs by enabling safe reduction of unnecessary PCT testing through two operating strategies:

Rule-out strategy — maximizes sensitivity and NPV to safely defer PCT testing
Balanced strategy — maximizes overall diagnostic performance for routine clinical deployment

The pipeline was developed and internally validated on a development cohort, then externally validated on an independent dataset with locked models and locked thresholds.

Clinical Context
Procalcitonin is a biomarker used to guide antibiotic therapy, particularly in sepsis and respiratory infections. However, routine PCT testing incurs unnecessary costs and delays when ordered indiscriminately. This pipeline predicts whether a patient's PCT is likely to be elevated (≥ 0.5 ng/mL) using only CBC and CRP parameters available at the time of initial assessment, enabling:

Safe deferral of PCT testing in low-risk patients (rule-out strategy)
Prioritization of high-risk patients for immediate PCT measurement
Support for antimicrobial stewardship and cost containment


Models Implemented
ModelTypeKey Hyperparameters TunedRandom ForestEnsemble (bagging)n_estimators, max_depth, min_samples_split, class_weightXGBoostEnsemble (boosting)learning_rate, max_depth, subsample, scale_pos_weightSVMKernel-basedC, gamma, kernel, class_weightLogistic Regression
