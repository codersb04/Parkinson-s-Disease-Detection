# Parkinson-s-Disease-Detection
## Task:
Build a model to predict whether a person has Parkinson's Disease.</br>
This problem comes under supervised learning as labelled data is given.</br>
A support Vector Machine(SVM) Classifier Algorithm is implemented for the prediction.

## Dataset:
The dataset is taken from Kaggle's "Parkinson's Disease Detection Dataset". The dataset contains 195 records with 24 features. The features are:
- name - ASCII subject name and recording number
- MDVP:Fo(Hz) - Average vocal fundamental frequency
- MDVP:Fhi(Hz) - Maximum vocal fundamental frequency
- MDVP:Flo(Hz) - Minimum vocal fundamental frequency

Five measures of variation in Frequency: 
- MDVP:Jitter(%) - Percentage of cycle-to-cycle variability of the period duration
- MDVP:Jitter(Abs) - Absolute value of cycle-to-cycle variability of the period duration
- MDVP:RAP - Relative measure of the pitch disturbance
- MDVP:PPQ - Pitch perturbation quotient
- Jitter:DDP - Average absolute difference of differences between jitter cycles

Six measures of variation in amplitude:
- MDVP:Shimmer - Variations in the voice amplitdue
- MDVP:Shimmer(dB) - Variations in the voice amplitdue in dB
- Shimmer:APQ3 - Three point amplitude perturbation quotient measured against the average of the three amplitude
- Shimmer:APQ5 - Five point amplitude perturbation quotient measured against the average of the three amplitude
- MDVP:APQ - Amplitude perturbation quotient from MDVP
- Shimmer:DDA - Average absolute difference between the amplitudes of consecutive periods

Two measures of ratio of noise to tonal components in the voice: 
- NHR - Noise-to-harmonics Ratio and 
- HNR - Harmonics-to-noise Ratio

Target:
- status - Health status of the subject (one) - Parkinson's, (zero) - healthy

Two nonlinear dynamical complexity measures:
- RPDE - Recurrence period density entropy
- D2 - correlation dimension
- DFA - Signal fractal scaling exponent

Three nonlinear measures of fundamental frequency variation:
- spread1 - discrete probability distribution of occurrence of relative semitone variations
- spread2 - Three nonlinear measures of fundamental frequency variation
- PPE - Entropy of the discrete probability distribution of occurrence of relative semitone variations</br></br>

Source: https://www.kaggle.com/datasets/naveenkumar20bps1137/parkinsons-disease-detection

## Steps Involved:
### Import Dependencies:
Libraries needed to achieve the task:

 - numpy
 - pandas
 - train_test_split from sklearn.model_selection
 - StandardScaler from sklearn.preprocessing
 - svm from sklearn
 - accuracy_score from sklearn.metrics

### Data Collection and Analysis:
- Load the data using read_csv function of pandas.
- Make use of function shape, info, isnull and describe to analyse the data.
### Data Preprocessing:
- Split the data into Target and Feature. Target will only contain the status column which depicts 1(Person has Parkinson's Disease) or 0(Person is healthy) and Features will have the rest of the column except for name(as it is hard to process by computer) and status.
- Standardize the data using the Standard Scaler class.
### Splitting the data into Train and test sets:
- Split the data as 20% for test and 80% for training
### Model Training
- Used Support Vector Classified to build the model
### Model Evaluation:
- Model is Evaluated for both the trained and test data
- Accuracy score of trained data:  0.8846153846153846
- Accuracy score of test data:  0.8461538461538461
### Build a Predictive System:
- Take a random row from the data set
- Convert it to numpy array and reshape it as 2d array.
- Standardize the data in the array
- predict the data using the model built.</br></br></br>

Reference: Project 14. Parkinson's Disease Detection using Machine Learning - Python | Machine Learning Project, Siddhardhan, https://www.youtube.com/watch?v=HbyN_ey-JVc&list=PLfFghEzKVmjvuSA67LszN1dZ-Dd_pkus6&index=14
