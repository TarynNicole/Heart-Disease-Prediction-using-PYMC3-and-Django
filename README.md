# Heart-Disease-Prediction-using-PYMC3-and-Django
Repository for Advanced Machine Learning Project: Predicting heart disease for patient using PYMC3 and Django
Heart disease is a prevalent problem in health care and requires the automation of classifying heart disease in patients. This speeds up the diagnosis process which saves lives as diagnosing it too late could be fatal.

Thus the problem can be defined as predicting whether a patient suffers from heart disease or not based on the Cleveland UCI dataset.

Objectives:
1. Analyze data to better understand the data and how to tackle the problem.
2. Create a probabilistic model using Python and PYMC3 for predicting whether a patient suffers from heart disease or not.
3. Create a web framework using Django for deployment of the model, providing a UI for hospitals and doctors. The patient info will simply be fed into the system and it will return their results automatically, with its measurement of certainty/uncertainty.

# Why Probabalistic Machine Learning?
Probabailistic models incorporate random variables and probability distributions into the model of an event or phenomenon. While a deterministic model gives a single possible outcome for an event, a probabilistic model gives a probability distribution as a solution. These models take into account the fact that we can rarely know everything about a situation. There’s nearly always an element of randomness to take into account.

Probabilistic programming (PP) allows flexible specification of Bayesian statistical models in code.

It also avoids data overfitting and provides easily interpretable models.

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

## Requirements and Resources

Python Version: 3.9.2
Packages: pandas, numpy, seaborn, sklearn, matplotlib, pickle, pymc3, arviz, django, django-widget-tweaks
Dataset: https://archive.ics.uci.edu/ml/datasets/heart+disease
Heart Disease: https://www.onhealth.com/content/1/heart_disease_coronary_artery

## Example Exploratory Analysis
![image](https://github.com/TarynNicole/Heart-Disease-Prediction-using-PYMC3-and-Django/assets/70257895/e2d0040a-5ee1-4bbb-8a42-497dbd98560d)
![image](https://github.com/TarynNicole/Heart-Disease-Prediction-using-PYMC3-and-Django/assets/70257895/ffc46ec4-391a-42ae-895e-c7b687fe2988)

#PYMC3 Model:

![image](https://github.com/TarynNicole/Heart-Disease-Prediction-using-PYMC3-and-Django/assets/70257895/9dc53955-3b1c-4484-a68a-c9ce690f2479)

# Comparing metrics of Machine Learning Models:
## Decision Trees:

![image](https://github.com/TarynNicole/Heart-Disease-Prediction-using-PYMC3-and-Django/assets/70257895/ef75883d-479e-43ac-84b5-c4450502a3b4)


## KNN Classifier:
![image](https://github.com/TarynNicole/Heart-Disease-Prediction-using-PYMC3-and-Django/assets/70257895/bf3aae44-9e60-44ae-9952-b3878fb655e9)


## Support Vector Machine:

![image](https://github.com/TarynNicole/Heart-Disease-Prediction-using-PYMC3-and-Django/assets/70257895/16448af4-0fff-4f2e-8896-435c290cb550)


## PYMC3 (Probabilistic) Model:

![image](https://github.com/TarynNicole/Heart-Disease-Prediction-using-PYMC3-and-Django/assets/70257895/cae6ede2-178f-4c1e-9a3c-30faa7016a6f)


As can be seen, the probabalistic model created performs well compared to the other 3 classifiers across all metrics. The probabalistic model's benefits have already being explained above. We can note that it also performs well for both classes (has disease and does not have disease). It also has an overall acccuracy of 87% which is quite high, making it reliable.

Probabilistic Model is also the best to use since heart disease diagnosis is a very sensitive area and requires a measurement of uncertainty for medical experts to properly consult the system when using diagnosis. This means that it provides extra caution to the diagnosis process.

