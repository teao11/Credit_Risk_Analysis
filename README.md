# Credit_Risk_Analysis

# Overview of the Analysis
In this module, we were leveraging our knowledge of supervised machine learning to predict credit risk. We utilized multiple models to compare the results, so that we could either move forward with the best model or via another route.

We utilized Resampling Models, the SMOTEENN Algorithm and even Ensemble Classifiers in order to predict credit risk using our training data.

## Naive Random Oversampling

![Screen Shot 2021-10-08 at 12 39 01 AM](https://user-images.githubusercontent.com/46773181/136517251-02c19cc1-59be-4e50-8c49-aeba25a479dc.png)

![Screen Shot 2021-10-08 at 12 39 13 AM](https://user-images.githubusercontent.com/46773181/136517273-e1108423-5bd0-4ab3-b05d-c45194caa622.png)

- Very bad at classifying high, but much better at classifying low risk in terms of precision
- Recall was around the same, however F1 showed differences between classifying the two
- In terms of using this model, it would depend on whether we are okay missclassifying lows as high (this makes sense given the use case)

## Smote Oversampling

![Screen Shot 2021-10-08 at 12 39 29 AM](https://user-images.githubusercontent.com/46773181/136517302-aa21beca-731a-40d3-8654-2d402e20653a.png)

![Screen Shot 2021-10-08 at 12 39 38 AM](https://user-images.githubusercontent.com/46773181/136517324-1a50c9de-9566-46e9-a792-7e59d871031e.png)

- Seems pretty in line with the model before it in terms of precision
- Recall slightly worse for high risk using smote than the model prior
- All in all not much difference to the one before

## Undersampling

![Screen Shot 2021-10-08 at 12 39 57 AM](https://user-images.githubusercontent.com/46773181/136517370-c6c5e34f-6e6b-461d-b228-f6c96f1209e4.png)

![Screen Shot 2021-10-08 at 12 40 14 AM](https://user-images.githubusercontent.com/46773181/136517406-9aea661d-3c00-49dd-adbb-1946848e1934.png)

- Similar in terms of precision to the first two, however the recall is much worse on the side of low risk (more misclassified here)
- F1 score is worse than the first two, would definitely punt on this model

## Combination

![Screen Shot 2021-10-08 at 12 40 31 AM](https://user-images.githubusercontent.com/46773181/136517439-0b9c58bd-3284-43ae-abe3-957afd9b4355.png)

![Screen Shot 2021-10-08 at 12 40 41 AM](https://user-images.githubusercontent.com/46773181/136517456-10b3320f-83b2-4e9e-be9d-83d32b471b82.png)

- Similar in terms of precision
- Recall is slightly greater than the first three in terms of recall for high risk (more accurate within the category), and slightly lower for the first two models in terms of low risk recall
- Better at classifying high risk than the first three, but I think this loses to much accuracy at the low end which seems less ideal

# Balanced Random Forest Classifier

![Screen Shot 2021-10-08 at 12 41 38 AM](https://user-images.githubusercontent.com/46773181/136517595-9a9bdb5e-fdb6-4032-b5e8-4f3a9114f65c.png)

![Screen Shot 2021-10-08 at 12 41 48 AM](https://user-images.githubusercontent.com/46773181/136517611-12a0a8b8-be3c-449b-853b-a8da0a5bbc90.png)

- 3x improvement on the high risk precision, and far greater recall for the low risk candidates which definitely seems ideal
- Predicted low / actual high is also reduced
- This is a likely candidate after viewing the first four

# EasyEnsembleClassifier

![Screen Shot 2021-10-08 at 12 42 12 AM](https://user-images.githubusercontent.com/46773181/136517669-89b32785-5a10-43bd-8c27-3a383f36d6a1.png)

![Screen Shot 2021-10-08 at 12 42 21 AM](https://user-images.githubusercontent.com/46773181/136517694-0c705570-993d-4957-81e8-f0976ad2ddd3.png)

- This is the best model we have looked at
- Precision is better for both labels
- very few misscategorized low's from our training data and wrongly predicted low's are also reduced
- I would definitely suggest moving forward here

# Summary

Given my comparisons above, I believe htat the Easy Ensemble Classifier is the best candidate to utilize!





