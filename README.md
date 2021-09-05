# Male Female Detector (Profiling)
The Main Objective of this EDA and Machine Learning is to provide a Profiling Data for Crime Division of Police Department to make it easier to find the suspects of crime.

**1. Initial Hypothesis and EDA**
- Long Hair will affect the Gender
- Forehead Width will affect the Gender
- Forehead Height will affect the Gender
- Nose Wide will affect the Gender
- Nose Long will affect the Gender
- Lips Thin will affect the Gender
- Distance nose to lip will affect the Gender

![Long Hair](https://github.com/tommysachi/Gender-Profiling/blob/main/Table%20%26%20Visual/Long%20Hair%20VS%20Gender.JPG)

![Forehead Width](https://github.com/tommysachi/Gender-Profiling/blob/main/Table%20%26%20Visual/Forehead%20Width%20VS%20Gender.JPG)

![Forehead Height](https://github.com/tommysachi/Gender-Profiling/blob/main/Table%20%26%20Visual/Forehead%20Height%20VS%20Gender.JPG)

![Nose Wide](https://github.com/tommysachi/Gender-Profiling/blob/main/Table%20%26%20Visual/Nose%20Wide%20VS%20Gender.JPG)

![Nose Long](https://github.com/tommysachi/Gender-Profiling/blob/main/Table%20%26%20Visual/Nose%20Long%20VS%20Gender.JPG)

![Lips Thin](https://github.com/tommysachi/Gender-Profiling/blob/main/Table%20%26%20Visual/Lips%20Thin%20VS%20Gender.JPG)

![Distance Lips to Nose](https://github.com/tommysachi/Gender-Profiling/blob/main/Table%20%26%20Visual/Distance%20Nose%20Lip%20VS%20Gender.JPG)

**2. Machine Learning Base Model**

The Algorithm that we used:

- Logistic Regression
- KNN (KNN Classifier)
- SVM (SVC)

The Summary of the Evaluation Matrix :

![Evaluation Matrix](https://github.com/tommysachi/Gender-Profiling/blob/main/Table%20%26%20Visual/Evaluation%20Matrix%20Summary.JPG)

The Accuracy Score was 0.97, which is already too good.

**3. Optimization**

Using Manual Tuning, we try to optimize the Error of the Machine Learning SVM Model.

Tuning From C = 1 to C =200, with Max Iterations = 400

![Tuning](https://github.com/tommysachi/Gender-Profiling/blob/main/Table%20%26%20Visual/Tuning.JPG)

With The Evaluation Matrix, increasing 0.006 (accuracy score)

![Optimized Evaluation Matrix](https://github.com/tommysachi/Gender-Profiling/blob/main/Table%20%26%20Visual/Evaluation%20Matrix%20Optimized.JPG)

**4. Conclusion and Simulation**

This Model will have 97% chance to predict right gender based on face data.

Simple Simulation :
```
SVM_Scaled.predict([[0,1,1,0,1,4,3]])[0]
```
will predict MALE

```
SVM_Scaled.predict([[1,0,1,0,0,2,2]])[0]
```
will predict FEMALE