# Covid-19-Detection-using-CNN
Project Description:
This project aims to develop a COVID-19 detection system using a Convolutional Neural Network (CNN). The goal is to classify chest X-ray images as either COVID-19 positive or negative. The CNN model is trained on a dataset consisting of COVID-19 positive images, COVID-19 mask images, normal images, and normal mask images. The dataset is preprocessed, and the images are resized and normalized before feeding them into the model. The trained model is then evaluated using a test set to measure its accuracy in correctly classifying COVID-19 cases. The project also includes a functionality to classify new chest X-ray images by providing the image path as input, allowing users to easily determine if a given image indicates a COVID-19 infection or not.

WHY CNN?
CNNs are preferred for image-related tasks due to their ability to capture local patterns, exploit parameter sharing, and perform hierarchical feature extraction, making them highly effective and efficient for image classification and analysis when compared with other neural networks.


Coding interfaces:
interactive python notebook
You can use Google Colab or Jupyter notebook for the code execution.


Model Architecture:
The CNN model used in this project consists of multiple layers designed to extract meaningful features from the input images and make predictions. The architecture of the model is as follows:
1.Convolutional Layers:
    -->The model starts with a Conv2D layer with 32 filters and a 3x3 kernel size, using the ReLU activation function.
    -->This is followed by a MaxPooling2D layer to downsample the spatial dimensions.
    -->Two more Conv2D layers with 16 filters and a 3x3 kernel size are added, each followed by a MaxPooling2D layer.
2.Flatten Layer:
    -->After the convolutional layers, a Flatten layer is used to convert the 2D feature maps into a 1D feature vector.
3.Dense Layers:
    -->The flattened features are passed to two Dense layers with 512 and 256 units, respectively, using the ReLU activation function.
    -->The final Dense layer consists of a single unit with a sigmoid activation function, which outputs the predicted probability of the        input image belonging to the positive class (COVID-19).
    
The model is compiled with the Adam optimizer and the BinaryCrossentropy loss function, as it is a binary classification problem. The accuracy metric is also specified for evaluation during training.
