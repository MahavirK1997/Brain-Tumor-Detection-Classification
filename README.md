# Brain-Tumor-Detection-Classification

## Overview
This project involves detecting and classifying brain tumors using a Convolutional Neural Network (CNN) model. The CNN was trained to classify four types of brain conditions: glioma, meningioma, no-tumor, and pituitary images. The project utilized both custom CNN architecture and transfer learning techniques with VGG19 and ResNet50 to enhance model accuracy and generalization.

## Dataset
The dataset used in this project was sourced from Kaggle: [Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset).

- **Training Data**:
  - Glioma: 1,321 images
  - Meningioma: 1,339 images
  - No Tumor: 1,595 images
  - Pituitary: 1,457 images

- **Testing Data**:
  - Glioma: 300 images
  - Meningioma: 306 images
  - No Tumor: 405 images
  - Pituitary: 300 images

- **Validation Data**:
  - Split: 50% split from testing data

- **Normalization**: 
  - Pixel values were normalized by dividing by 255.

## CNN Model Architecture
The custom CNN model was built following a reference paper. The architecture includes:
- **5 Convolutional Blocks**: Each block has multiple convolutional layers followed by a max-pooling layer.
- **3 Dense Layers**: Used for classification.
- **Output Layer**: Number of nodes is equal to the number of classes (4).

### Training
- **Epochs**: 30 epochs
- **Training Accuracy**: 99%
- **Validation Accuracy**: 95%

## Image Augmentation
To improve model generalization and reduce overfitting, image augmentation was applied. Each training image was augmented to create 5 variations, including zoom-in, zoom-out, and rotation. Blurring and other methods that might cause loss of important information were avoided.

- **Training Accuracy (Post-Augmentation)**: 97%
- **Testing Accuracy**: 95%

## Transfer Learning
Pre-trained models VGG19 and ResNet50 were used for transfer learning.

### VGG19
- **Modifications**: Last 5 layers were unfrozen, and dense layers were added according to the model requirements.
- **Epochs**: 20 epochs
- **Training Accuracy**: 99%
- **Validation Accuracy**: 98%

### ResNet50
- **Modifications**: Unfrozen up to the last convolutional layer, added dense layers as required.
- **Epochs**: 30 epochs
- **Training Accuracy**: 95%
- **Validation Accuracy**: 94%

## Conclusion
This project successfully developed a model for brain tumor detection and classification with high accuracy. The use of image augmentation and transfer learning with VGG19 and ResNet50 significantly improved the model's performance and generalization capabilities. 

## Acknowledgments
Special thanks to Kaggle for providing the dataset.
