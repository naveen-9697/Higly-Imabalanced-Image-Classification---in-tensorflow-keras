# Imabalanced-classification-in-keras-for-15-classes

## What:
This is me practicing how to tackle a imbalanced multi-class image classification problem and this is about classifying 45,000 images of 15 different fruits.

## About:
<ol>
    <li>data can be found <a href=https://www.kaggle.com/chrisfilo/fruit-recognition>here on Kaggle</a>.</li>
    <!--
    <li></li>
    <li>Multi-Logloss was used as loss.</li>
    -->
    <li>How was the imbalance handled/tackled:</li>
    <ol>
        <li>I didn't get more data, albeit lots of images of fruits being available on the internet, to avoid input shift.</li>
        <li>I have augmented the images at every epoch, to ensure that the model has seen every various variations of every input image. e.g.: from various angles.</li>
        <li>By setting class weights, in other words, telling algorithm to pay extra attention to under represented classes.</li>
        <li>For proper judgement, stratified splits with equal proportions of images belonging to all classes were included in train, validation and test sets.</li>
        <liUsing an evaluation metric like Weighted harmonic mean, to judge the model's output better. And I have also used Recall to be extra sure.></li>
    </ol>
</ol>

## Data:
45,000 images of 15 different fruits can be <a href=https://www.kaggle.com/chrisfilo/fruit-recognition>found on kaggle</a>.
