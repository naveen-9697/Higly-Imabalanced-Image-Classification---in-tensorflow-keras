# Imabalanced-classification-in-keras-for-15-classes

## About:
This is an imbalanced multi-class classification problem.

## Data:
45,000 images of 15 different fruits can be <a href=https://www.kaggle.com/chrisfilo/fruit-recognition>found on kaggle</a>.

## About:
1. Data was imbalanced, so stratified splits with equal proportions of all classes has to be included in train and validation.
2. Multi-Logloss was used as loss.
3. Data was imbalanced, so multiple evaluation metrics had to be chosen. In the notebook, I have calculated:  
    a. <u>Primary evaluation metric</u>: <i>Weighted harmonic mean</i> using <a href='https://www.tensorflow.org/addons/api_docs/python/tfa/metrics/FBetaScore'><i>F-beta score</i></a>, that gives equal weights to all classes(with average='macro') has been used.  
    b. Accuracy using <a href='https://www.tensorflow.org/api_docs/python/tf/keras/metrics/CategoricalAccuracy'><i>CategoricalAccuracy</i></a>  
    c. Average <b>Precision</b> and <b>Recall</b> has also been calculated.  
4. To not have the weights of CNNs update for oversampled classes, additonal class weights have been supplied to let the algorithm give extra weight to under-sampled classes, which actually gave very good results.
