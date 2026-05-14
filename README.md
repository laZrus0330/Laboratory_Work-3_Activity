# Laboratory_Work-3_Activity

*Here is my Google Drive Folder:* [**Click Here!**](https://drive.google.com/drive/folders/1GuZnbRgpvgtdK60dkLpgWg7pxGr18xgN?usp=sharing)

*Here is my Google Colab:* [**Click Here!**](https://drive.google.com/drive/folders/1GuZnbRgpvgtdK60dkLpgWg7pxGr18xgN?usp=sharing)
---

# Guide Questions (Student Reflection & Explanation)

# 1. Dataset Preparation

## How did you organize your dataset in Google Drive?

I organized the dataset inside a main folder called `ImageDataset`. Inside this folder, I created 20 separate subfolders, where each folder represented one plant species such as `mango`, `durian`, and other plants. All images belonging to a specific class were placed inside their corresponding folders. This organization made the dataset easier to manage and helped TensorFlow automatically recognize the labels of each image.

## Why is folder structure important for TensorFlow image loading?

Folder structure is important because TensorFlow uses the folder names as the labels for the images when using `image_dataset_from_directory`. By organizing the dataset properly, TensorFlow can automatically classify images into their correct categories without manually assigning labels. It also makes the dataset cleaner, more organized, and easier to process during training.


# 2. Model Training

## What is the role of convolutional layers in image classification?

Convolutional layers are responsible for extracting important features from images. They detect patterns such as edges, textures, colors, and shapes. In the earlier layers, the model learns simple patterns, while deeper layers learn more complex features that help identify the plant species correctly.

## Why do we split data into training and validation sets?

The dataset is split into training and validation sets so the model can be evaluated properly.

- **Training Set** – Used for teaching the model and updating its weights.
- **Validation Set** – Used to test how well the model performs on images it has not seen before.

This is important because it helps determine whether the model is learning correctly or simply memorizing the training data.


# 3. Performance Analysis

## What accuracy did your model achieve?

The model achieved:

- **Training Accuracy:** 98.6%
- **Validation Accuracy:** 35.5%

The training accuracy was very high, but the validation accuracy was much lower. This means the model performed very well on the training data but struggled when predicting unseen images, which is a sign of overfitting.

## How did the number of images affect the model’s performance?

The number of images greatly affected the model’s performance. Although having around 300 images per class was enough to start training, the dataset still needed more image variety. Since there were 20 classes, the model required more diverse images with different lighting conditions, angles, and backgrounds to improve its ability to generalize.



# 4. Critical Thinking

## What challenges did you encounter while using your own dataset?

One challenge I encountered was the inconsistency in image quality, lighting, and backgrounds. Some images were clearer than others, which affected the training process. Another challenge was overfitting, where the model became too focused on the training images and could not perform well on validation data. Training also took a long time because of the large number of images and classes.

## How can data augmentation improve your model?

Data augmentation improves the model by creating modified versions of the existing images through random flips, rotations, zooms, and other transformations. This increases the diversity of the dataset and helps the model learn more generalized features instead of memorizing images. As a result, the model becomes more accurate on unseen data.



# 5. Application

## Suggest a real-world application for your trained model.

A possible real-world application for this model is a mobile application that can identify plant species using a camera. Farmers, students, or agricultural workers could use the app to quickly recognize plants or monitor crop conditions in the field.

## How can this system be integrated into a mobile or web application?

The system can be integrated into mobile and web applications in different ways:

- **Mobile Application:** The trained model can be converted into TensorFlow Lite (`.tflite`) format so it can run directly on smartphones.
- **Web Application:** The model can be connected to a backend using Flask or FastAPI and accessed through a website.
- **Browser-Based System:** TensorFlow.js can also be used to run the model directly inside a web browser.

---

# Activity 3A Guide Questions (Student Explanation & Reflection)


# 1. Visualization & Overfitting

## What signs indicated overfitting in your first model?

The first model showed overfitting because the training accuracy became very high while the validation accuracy remained low. This indicated that the model memorized the training images instead of learning patterns that could work on new images.

## How did data augmentation affect validation accuracy?

Data augmentation helped improve the validation accuracy because it exposed the model to different variations of the images. By seeing flipped, rotated, and zoomed images during training, the model became more flexible and performed better on unseen data.



# 2. Model Improvement

## What is the purpose of dropout layers?

Dropout layers help reduce overfitting by randomly turning off some neurons during training. This prevents the model from depending too much on certain neurons and forces it to learn more balanced and generalized features.

## Why does data augmentation improve generalization?

Data augmentation improves generalization because it increases the variety of training images without needing additional data collection. The model learns to recognize objects even when images are changed slightly, making it more reliable in real-world situations.



# 3. Performance Comparison

## Compare accuracy before and after improvements.

Before applying improvements, the model achieved high training accuracy but poor validation accuracy, which showed overfitting. After adding techniques such as data augmentation and dropout layers, the validation performance improved and the gap between training and validation accuracy became smaller.

## Which technique contributed most to improvement?

Data augmentation contributed the most because it increased the diversity of the training dataset. This helped the model learn more generalized patterns and improved its performance on validation images.



# 4. Deployment & Application

## Why is saving the model important?

Saving the model is important because it allows the trained neural network to be reused later without retraining it again. The saved model can be loaded for testing, prediction, deployment, or further improvements.

## How can this model be deployed in a real-world system?

The model can be deployed in real-world systems through:

- **Mobile Applications** using TensorFlow Lite for on-device predictions.
- **Web Applications** using Flask or FastAPI as backend services.
- **Browser-Based Systems** using TensorFlow.js to run the model directly in a browser.

This allows users to upload or capture images and receive instant predictions from the trained model.
