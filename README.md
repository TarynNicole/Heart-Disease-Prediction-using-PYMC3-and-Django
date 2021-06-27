# Heart-Disease-Prediction-using-PYMC3-and-Django
Repository for Advanced Machine Learning Project: Predicting heart disease for patient using PYMC3 and Django
Heart disease is a prevalent problem in health care and requires the automation of classifying heart disease in patients. This speeds up the diagnosis process which saves lives as diagnosing it too late could be fatal.

Thus the problem can be defined as predicting whether a patient suffers from heart disease or not based on the Cleveland UCI dataset.

Objectives:
1. Analyze data to better understand the data and how to tackle the problem.
2. Create a probabilistic model using Python and PYMC3 for predicting whether a patient suffers from heart disease or not.
3. Create a web framework using Django for deployment of the model, providing a UI for hospitals and doctors. The patient info will simply be fed into the system and it will return their results automatically, with its measurement of certainty/uncertainty.

## Description of Heart Dataset
----
The full dataset contains 76 attributes. However, for the purposes of this project, only a subset of 14 attributes will be utilized. The 'num' field is our target field, which indicates the presence of heart disease in the pateint. 
For ethical purposes, the names and any other personal information of the patients were not included in the dataset.

Below is the attribute information of the dataset being utilized:
<br/>
1. **Age**: Age in years
2. **Sex**: (1=male, 0=female)
3. **CP**: Chest pain type 
   <br/>(1 = typical angina, 2 = atypical angina, 3= non-anginal pain, 4 = asymptomatic)
4. **trestbps**: Resting blood pressure in mm Hg on admission to hospital
5. **chol**: Serum cholestoral in mg/dl
6. **fbs**: Fasting blood sugar > 120 mg/dl (1=true, 0=false)
7. **restecg**: Resting electrocardiographic results 
   <br/>(0=normal, 1=having ST-T wave abnormality, 2=showing probable or definite left ventricular hypertrophy by Estes' criteria)
8. **thalach**: Max heart rate achieved (actual value).
9. **exang**: Exercise induced angina (1=yes, 0=no)
10. **oldpeak**: ST depression induced by exercise relative to rest
11. **slope**: Slope of peak exercise ST segment
    <br/>(1=unsloping, 2=flat, 3=downsloping)
12. **ca**: Number of major vessels (0-4) coloured by flourosopy
13. **thal**: Maximum heart rate achieved (ordinal)
14. **target**: diagnosis of heart disease (0,1)
