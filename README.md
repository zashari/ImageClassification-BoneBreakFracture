# Image Classification on Bone Break Fracture Images

### Introduction

This is my personal project, I embarked on a comprehensive project focused on developing an image classification model for identifying different types of bone fractures from radiographic images. This project involved a series of complex tasks, including data preprocessing, model training, and validation, leveraging deep learning techniques and computer vision.

### Data Pre-processing

#### Dataset Organization
The dataset comprised images of various types of bone fractures, such as spiral, pathological, oblique, and more. These were organized into separate folders for each fracture type, forming the basis of our classification categories.

#### Image Analysis
An initial analysis of the dataset revealed a total of 1,257 images spread across 12 fracture categories. The images were primarily in JPEG and PNG formats. To ensure consistency, I removed images in non-standard formats like GIF and WEBP.

#### Color Analysis and Duplication Handling
I implemented a function to calculate the color count of each image, aiding in understanding their complexity. Furthermore, I used the cosine similarity technique to identify and remove duplicate images, ensuring the uniqueness of the dataset.

#### Feature Extraction with MobileNetV2
Using the pre-trained MobileNetV2 model, I extracted features from each image, converting them into a 1000-dimensional embedding space. This reduced representation was crucial for subsequent analysis and model training.

### Model Development and Training

#### Data Cleaning and PCA
I applied Principal Component Analysis (PCA) to reduce the dimensionality of our embeddings, making the data more manageable for processing. Additionally, I employed Isolation Forest for outlier detection, flagging and removing anomalous images that could potentially skew the model's performance.

#### Preparing the Dataset
The cleaned dataset was then divided into training and testing sets. I applied various image transformations, such as resizing, random cropping, horizontal flipping, and normalization, to augment the data and improve the model's generalization ability.

#### Model Architecture and Training
For the classification task, I utilized a pre-trained ResNet-18 model, adapting its final layer to match the number of fracture classes. The model was trained on a GPU for enhanced performance, using the Adam optimizer and Cross-Entropy Loss as the learning criterion.

Over 25 epochs, the model's training and validation losses were monitored, along with its accuracy on the test set. The model showed steady improvement, with a final accuracy of 77% on the test dataset, indicating its capability to classify different types of bone fractures effectively.

### Conclusion

This project was a challenging yet rewarding experience, allowing me to apply my theoretical knowledge in deep learning and computer vision to a practical scenario. The successful development of a bone fracture classification model not only enhanced my understanding of image processing and neural networks but also underscored the potential of AI in medical imaging. This project, as part of my academic journey, significantly contributed to my skills in data science and machine learning.
