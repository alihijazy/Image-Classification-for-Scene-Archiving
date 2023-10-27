# Image Classification for Scene Archiving

## Overview

This project aims to create an image archiving model that classifies images into six different types of scenes. The model is designed to help automate the process of categorizing images for efficient archiving.

## Dataset

### Context
This Data contains around 17k images of size 150x150 distributed under 6 categories. This dataset was originally published on [Analytics Vidhya](https://datahack.analyticsvidhya.com) by Intel for an image classification challenge.

### Content
- Approximately 17,000 images
- Image size: 150x150 pixels
- Distributed under six categories:
    - 'Buildings' -> 0
    - 'Forest' -> 1
    - 'Glacier' -> 2
    - 'Mountain' -> 3
    - 'Sea' -> 4
    - 'Street' -> 5

### Data Split
- Training Data: ~14,000 images
- Test Data: ~3,000 images


## Business Problem

The project addresses the need for efficient image archiving. By automating scene classification, this tool can save time and enhance the organization of large collections of photographs.
The inspiration behind this project is to build a powerful neural network capable of accurately classifying images, which can have applications in various domains requiring image categorization.


## Methods

The best performing model in this project was a neural network model of the below architecture:  

- `Conv2D(filters=32, kernel_size=(3, 3))`
- `MaxPooling2D(pool_size=(3, 3))`
- `Conv2D(filters=64, kernel_size=(3, 3))`
- `MaxPooling2D(pool_size=(2, 2))`
- `Conv2D(filters=128, kernel_size=(3, 3))`
- `MaxPooling2D(pool_size=(2, 2))`
- `Conv2D(filters=256, kernel_size=(3, 3))`
- `MaxPooling2D(pool_size=(2, 2))`
- `Conv2D(filters=512, kernel_size=(3, 3))`
- `Conv2D(filters=1024, kernel_size=(3, 3))`
- `Flatten()`
- `Dense(filters=1024)`
- `Dense(filters=6)`

### Model performance
The model scored 87% accuracy on the training data and 86% accuracy on the test data, with a validation loss of 0.4.  
#### Accuracy and Loss  
![Alt Text](C:\Users\alihi\Documents\Flatiron\Phase 4\project\kaggle\images\model_3_Accuracy_and_loss.png)

#### Confusion matrix

## Recommendations
1. **Implementation of the Image Classification Model:**
   - Begin the implementation of the image classification model for archiving purposes.

2. **Establish a Feedback Loop:**
   - Establish a feedback loop with archivists and users to continually improve the model's performance.

3. **Explore Partnerships and Collaborations:**
   - Explore partnerships and collaboration opportunities with organizations or platforms in related fields, such as content management or digital libraries.

## Future Enhancements

To further improve the utility of this tool for image archiving, consider the following enhancements:

1. **Multi-Label Classification:** Allow the model to assign multiple scene labels to images, accommodating cases where an image contains elements from multiple categories (e.g., "street," "car," "building").

2. **Additional Categories:** Expand the model's capabilities to classify images into more than six categories to cover a wider range of scenes.

3. **Image Metadata Integration:** Incorporate image metadata (e.g., location, date) to enhance archiving and retrieval capabilities.