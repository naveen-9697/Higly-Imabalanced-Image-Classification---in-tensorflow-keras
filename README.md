# Imabalanced-classification-in-keras-for-15-classes

## About the notebook:

1. Data was imabalanced, so splits with equal proportions of all classes has to be included in train and test.
2. Data was imabalanced, so multiple weighted evaluation metrics has to be chosen. I have calculated:  
    a. <u>Primary evaluation metric</u>: <i>Weighted harmonic mean</i> using <a href='https://www.tensorflow.org/addons/api_docs/python/tfa/metrics/FBetaScore'><i>F-beta score</i></a>, that gives equal weights to all classes(with average='macro') has been used.  
    b. Accuracy using <a href='https://www.tensorflow.org/api_docs/python/tf/keras/metrics/CategoricalAccuracy'><i>CategoricalAccuracy</i></a>  
    c. Average <b>Precision</b> and <b>Recall</b> has also been calculated.  
3. Becuase of the imbalance in the data, additonal class weights have been supplied to let the algorithm give extra weight to under-sampled classes.  
4. Xception with weights of 'imagenet' has been adopted without including top layers. At final layers, two additional fully connected layers with dropout of 0.5 has been added.
