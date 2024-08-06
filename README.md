# CNN_FlowerPred
This repository contains a machine learning model built with Convolutional Neural Networks (CNN) for predicting flower species from images. The model is trained on a dataset of flower images with corresponding labels of different flower species. I downloaded the data from a kaggle competition. It can be accessed using: </br>
https://drive.google.com/drive/folders/1YczEVJNQHzgzLrEJIE9puceFw96DtSJw?usp=drive_link
## Dataset
The dataset used for training and evaluating the model consists of a diverse collection of flower images. Each image in the dataset is labeled with the corresponding flower species, allowing the model to learn to distinguish between different types of flowers like, tulip, sunflower, rose, daisy, and dandelion. The dataset is split into training and validation sets to evaluate the model's performance and prevent overfitting.
## Model Architecture
The CNN architecture employed in this project is designed to capture the intricate features present in flower images. The model consists of multiple convolutional layers followed by max-pooling layers to extract and downsample the relevant features. The final layers include fully connected layers with 'relu' activation to produce the probability distribution over different flower species. The last layer has 5 outputs for each class of flower using softmax activation.</br>
Then later I used Resnet50, EfficientNet, and VGG pre-defined weights to train followed by some fully connected layers with 'relu' or 'sigmoid' activation.
## Image Data Generation
At first, I tried to write the function using some commonly used parameters for the function. It gave good accuracy for my basic CNN model but not for other models I used. So, I tried to use  tensorflow.keras.applications.resnet50.preprocess_input which boosted up my accuracy upto 88%.
## Model Training
I compiled the models using 'categorical_crossentropy' loss and 'adam' optimizer. Loss and accuracy were calculated for each epoch which is later plotted. I was able to run only 10 epochs because of hardware limitations.
## Accuracy
1. Basic CNN model: Best Validation Set Accuracy: 51.39%
2. Resnet50: Best Validation Set Accuracy: 88.35%
3. EfficientNet: Best Validation Set Accuracy: 87.24%
4. VGG16: Best Validation Set Accuracy: 82.53%
</br>
The resnet model is saved as .h5 file. It can be accessed using:</br>
https://drive.google.com/file/d/1DgoWYiU4oMgCktU-XjvdEIUFQ_3QxIzK/view?usp=sharing
