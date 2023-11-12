# ResNet50-Face-Recognition
## GENDER PREDICTION WITH FINE-TUNED RESNET-50 
📁 Created by: Elsa Nurul Hidayah, 2023

Dataset: http://bit.ly/dataset_proj1 

## Introduction

🔬 In the evolving world of technology, one of the advancements that will greatly support the operations of many sectors is Face Recognition. It is a powerful tool that may be used to improve security, improve quality, and even improve sales. In the context of Business, an exemplary real-world case is the usage of face recognition technology that will aid in collecting data for demographic purposes. These retailers can then use these valuable demographic data for face recognition to gender prediction to personalize the shopping experience, optimize inventory, and refine marketing strategies based on accurate gender predictions from visual data. The urgency for implementation is driven by the need for a competitive edge in an industry defined by dynamic consumer expectations. However, this project is not limited to the retail sector, other sectors can implement it for other purposes.

The specified face recognition task used in this project is the prediction of gender from an image, using several features and labelings to extract information and train the ResNet50 model, after being adjusted using two fine tunings scenarios, with the data used to train, validate, and test the model is CelebA.

1. Simple Fine Tuning
2. Increased hidden layers Fine Tuning

![](https://mmlab.ie.cuhk.edu.hk/projects/CelebA/intro.png)

## Getting Started

To run this project on your local machine using Google Colab connected to Google Drive, follow these systematic steps:

### Prerequisites

Before you begin, make sure you have the following prerequisites:

1. Google Colab account
2. Access to Google Drive
3. Dependencies (in the section below)

### Procedure

1. Open Google Colab and navigate to the notebook located in the project's directory.

2. Mount Google Drive within the Colab notebook by executing the following cell:

    ```python
    from google.colab import drive
    drive.mount('/content/drive')
    ```
3. Clone the repository to your google colab (recommended):

    ```bash
    git clone https://github.com/elsxnh/ResNet50-Face-Recognition.git
    ```

4. Install any necessary dependencies by following the instructions in the notebook.

5. Run the notebook cells sequentially to train and test your model.

By following these steps, you should be able to successfully run the project and understand the implemented features.

## The Result

### Model 1

**Architecture:**
  - Directly applies GlobalAveragePooling2D to the base model's output.
  - Adds a Dense output layer with a sigmoid activation.

**Performance Metrics:**
  - Accuracy on test: 0.9350
  - Loss on test: 0.1388

**Classification Report:**

           precision    recall  f1-score   support

      Female       0.93      0.98      0.96       115
        Male       0.97      0.91      0.94        85

    accuracy                           0.95       200
   macro avg       0.95      0.94      0.95       200
weighted avg       0.95      0.95      0.95       200

**Confusion Matrix:**

![Model 1 Confusion Matrix](https://github.com/elsxnh/ResNet50-Face-Recognition/blob/master/assets/Confusionmatrix_1.png)


**Training and Validation Metrics:**

![Model 1 Trainining and Validating Comparison](https://github.com/elsxnh/ResNet50-Face-Recognition/blob/master/assets/Comparison_Finetune1.png)


### Model 2

**Architecture:**
Sequentially adds multiple Dense layers, reducing the number of neurons gradually.
Includes a GlobalAveragePooling2D layer and a Flatten layer.

**Performance Metrics:**
Accuracy on test: 0.9500
Loss on test: 0.1302

**Classification Report:**

           precision    recall  f1-score   support

      Female       0.97      0.96      0.96       115
        Male       0.94      0.96      0.95        85

    accuracy                           0.96       200
   macro avg       0.96      0.96      0.96       200
weighted avg       0.96      0.96      0.96       200


**Confusion Matrix:**

![Model 2 Confusion Matrix](https://github.com/elsxnh/ResNet50-Face-Recognition/blob/master/assets/Confusionmatrix_2.png)

**Training and Validation Metrics:**

![Model 2 Trainining and Validating Comparison](https://github.com/elsxnh/ResNet50-Face-Recognition/blob/master/assets/Comparison_Finetune2.png)

## Dependencies

This project requires the updated Python version in Colab and the following Python libraries installed:

* Basic Libraries: [NumPy](http://www.numpy.org/), [Matplotlib](http://matplotlib.org/), [Seaborn](https://seaborn.pydata.org/)
* Deep-learning Frameworks: [Keras](https://keras.io/), [TensorFlow](https://www.tensorflow.org/)

📨 For any discussion kindly contact me here: elsanhy.en@gmail.com | Linked-In: https://www.linkedin.com/in/elsanurul/

