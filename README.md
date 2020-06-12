# Kaggle CoronaHack -Chest X-Ray-Dataset with fastAI
Source: https://www.kaggle.com/praveengovi/coronahack-chest-xraydataset

## Introduction
This is an attempt at implementing transfer learning on a CoronaHack -Chest X-Ray-Dataset to identify a patient with Covid19 just by looking at their chest X-ray results.

![Chest Xray](/images/chest-x-ray.png)

Looking at the X-Ray from a layman perspective, there is hardly any difference between the X-Ray images and the patient's condition. The Convolutional Neural Net (CNN) algorithm is able to take seemingly similar X-Ray images, identify patterns in them that is hidden to the naked eye and tell the conditions apart.

I am using resnet34 as a base model for transfer learning. I will be training using the Chest X-Ray-Dataset provided by folks at Kaggle. The model yield pretty acceptable result, considering there were only about 58 Chest X-Ray of Covid patients with most of them having other conditions. I am using a 80/20 train test split.

## Prediction Results
{'COVID-19 (Virus)': 0.6666666666666666,\
 'Normal': 0.9238095238095239,\
 'Pnemonia (Virus)': 0.6287625418060201,\
 'Pnemonia (bacteria)': 0.8342342342342343,\
 'SARS (Virus)': 0.0}

 ## Confusion Matrix
 array([[  8,   2,   1,   1,   0],\
       [  0, 291,  17,   7,   0],\
       [  1,  18, 188,  92,   0],\
       [  2,  14,  76, 463,   0],\
       [  1,   0,   0,   0,   0]])

