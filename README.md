# Land Use and Land Cover classification
Leveraging Sentinel-2 Satellite Data and Deep Learning for Enhanced Land Use and Land Cover Classification


## Abstract
Land use and land cover classification using satellite imagery is a critical area of research with significant applications in environmental monitoring, urban planning, agriculture, and disaster management. This project addresses the challenge of classifying land cover using the EuroSAT dataset, which consists of Sentinel-2 satellite images spanning 13 spectral bands and covering ten distinct land cover categories. 

We employ advanced deep learning techniques to analyze these images, focusing on three prominent convolutional neural network architectures: **ResNet50**, **DenseNet201**, and **VGG16**. Our approach includes preprocessing steps such as resizing, data augmentation, and transformation to enhance model robustness and performance. 

We assess the models based on accuracy, comparing our results with previous benchmarks and evaluating the impact of data augmentation. Our results demonstrate that ResNet50 outperforms DenseNet201 and VGG16 with a test accuracy of 93.4%, highlighting its effectiveness in capturing complex features through residual connections. 

This study provides insights into effective deep-learning approaches for satellite image classification and contributes to advancing methodologies for practical applications in various domains.

## Preprocessing

In this project, we employed several preprocessing techniques to ensure that the data was in the best possible form for training the models. The dataset used was the **EuroSAT** dataset, which contains RGB satellite imagery. First, we loaded and explored the dataset using TensorFlow Datasets (tfds) to better understand its structure, including the ten land cover categories present.

To prepare the images for training, we resized them to match the input dimensions required by each of the deep learning architectures we used. Additionally, we applied **data augmentation** techniques such as random flipping, rotation, and scaling to improve the generalization ability of the models. These transformations simulate variations in the data, helping the models become more robust and perform better on unseen data.

We split the dataset into three subsets: training, validation, and testing sets, using an 80/10/10 split. This split allows us to train the model effectively while also providing validation data to tune the model and test data to evaluate its final performance. Finally, we visualized a sample of images from the dataset to verify the preprocessing steps and gain insights into the land cover types.

## Models

We explore three different deep-learning architectures to classify the land cover:

1. **ResNet50**
2. **VGG16**
3. **DenseNet201**


### Model Comparison

The models were trained on the preprocessed EuroSAT dataset, and their performances were evaluated based on accuracy. Our experiments showed that:

- **ResNet50** achieved the highest test accuracy at **93.4%**.
- **DenseNet201** and **VGG16** showed competitive but lower performance.

Data augmentation played a significant role in improving the model performance across the board.

## Conclusion

The ResNet50 model's residual connections enable it to capture complex features in satellite imagery, making it the most effective model in this study. Data augmentation further enhances the generalization capability of the models, making them more robust in classifying different land cover types from satellite images. This project provides a foundation for future work in satellite image classification and has potential applications in areas like urban planning and environmental monitoring.


