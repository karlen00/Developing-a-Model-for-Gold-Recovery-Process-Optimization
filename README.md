# README

## Project: Developing a Model for Gold Recovery Process Optimization

### Project Description
You have access to data stored in three files:
- `gold_recovery_train.csv` — download the training dataset
- `gold_recovery_test.csv` — download the test dataset
- `gold_recovery_full.csv` — download the full dataset

This data is indexed by the date and time it was obtained (feature date). Parameters that are close in time are usually similar. Some parameters are unavailable because their measurements and/or calculations were done much later. Therefore, some features in the training set might not be present in the test set, and the test set does not contain the target variable.

The source dataset includes both the training and test sets with all features.

Remember, the data you have is raw and has just been downloaded from the data warehouse. Before creating a model, check the accuracy of your data. Follow the instructions below.

### Project Instructions

#### 1. Prepare the Data
1.1. Open the files and examine the data.
   - File paths:
     - `/datasets/gold_recovery_train.csv`
     - `/datasets/gold_recovery_test.csv`
     - `/datasets/gold_recovery_full.csv`

1.2. Verify if the gold recovery has been calculated correctly. Using the training set, calculate the recovery for the feature `rougher.output.recovery`. Find the MAE between your calculations and the feature values. Present your findings.

1.3. Analyze the features not available in the test set. What are these parameters? What types are they?

1.4. Perform data preprocessing.

#### 2. Analyze the Data
2.1. Note how the concentration of metals (Au, Ag, Pb) changes depending on the purification stage.

2.2. Compare the distribution of particle size in the feed between the training set and the test set. If the distributions vary significantly, the model evaluation will be incorrect.

2.3. Consider the total concentration of all substances at different stages: raw feed, rougher concentrate, and final concentrate. Do you observe any abnormal values in the total distribution? If so, should these values be removed from both samples? Explain your findings and remove anomalies if necessary.

#### 3. Develop the Model
3.1. Create a function to calculate the final sMAPE value.

3.2. Train different models. Evaluate these models using cross-validation. Select the best model and test it using the test sample.

### Data Description
The data includes features indexed by date and time. Some of the key features include:
- `date` — Date and time the data was recorded.
- `rougher.output.recovery` — The recovery rate of the rougher stage.

Other relevant features include concentrations of metals (Au, Ag, Pb) at various stages and particle size distributions.

### Steps Taken
1. **Data Preparation:**
   - Examined the data files and understood their structure.
   - Verified the calculation of gold recovery.
   - Analyzed unavailable features in the test set.
   - Preprocessed the data for further analysis.

2. **Data Analysis:**
   - Monitored changes in metal concentrations at different purification stages.
   - Compared particle size distributions between training and test sets.
   - Analyzed total concentrations at various stages and addressed any anomalies.

3. **Model Development:**
   - Created a function to calculate sMAPE.
   - Trained and evaluated different models using cross-validation.
   - Selected the best model and tested it on the test sample.

### Conclusion
This project involves preparing and analyzing raw data from a gold recovery process, developing models to predict recovery rates, and evaluating these models to select the best one for optimizing the process. The final model should provide accurate predictions to help improve the efficiency and profitability of the gold recovery process.
