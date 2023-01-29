# 545project

Based on dataset of anonymized chest x-ray images and classification labels from NIH, the project is mainly focus on combining machine learning with data analysis tools to realize Chest X-ray image classification. Meanwhile, we also performed some statistical data analysis from the result of model training. 

In Pre-trained EDA part, we implemented regular data preprocessing operations and One-Hot Encoding to processed text labels data. 

We built a CNN model to achieve the classification. We used Keras to build CNN model. The model has 4 stages and each stage has convolutional layer, max-pooling layer, batch normalization and dropout layer. We also used ReLU and sigmoid to flatten output state. The model’s kernel size is 3*3 and the batch size is 64. Finally, the loss converges is 0.3 and accuracy converges is 0.9.

We also used DenseNet121 model to improve converges. DenseNet121 can obtain additional inputs from preceding layers and passes its own feature-maps to all subsequent layers. The batch size is 8. The loss and accuracy still converge to 0.3 and 0.9 respectively.

Everything is implemented on AWS platform and we establish a sageMaker note with the type of ml.p2.8xlarge (100 GB for SSD and 128 RAM) and stored our trained model as h5 file.
