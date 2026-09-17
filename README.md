# Deep Learning – Fashion Image Classification

## Overview

This practical demonstrates how **Deep Learning** can be used to classify fashion product images.

The project uses the **Fashion MNIST dataset** and a simple **Artificial Neural Network (ANN)** to identify different types of fashion products.

The practical connects Deep Learning concepts with an **e-commerce business use case**, where AI can assist in automatically categorizing product images.

---

## Business Problem

An e-commerce company receives thousands of product images that need to be categorized.

Instead of manually classifying every image, a Deep Learning model can analyze an image and predict its product category.

### Example Categories

* T-shirt / Top
* Trouser
* Pullover
* Dress
* Coat
* Sandal
* Shirt
* Sneaker
* Bag
* Ankle Boot

### Business Flow

```text
Product Image
      ↓
Deep Learning Model
      ↓
Predicted Category
      ↓
Human Review
      ↓
Product Listing
```

---

## Learning Objectives

The practical helps us understand:

* How images can be used as input for Deep Learning.
* How an Artificial Neural Network works.
* The purpose of input, hidden, and output layers.
* How image data is prepared for training.
* How a neural network is trained.
* How model accuracy is measured.
* How a trained model makes predictions.
* How image classification can be applied in e-commerce.
* Why human review may still be required.

---

## Dataset

The project uses the **Fashion MNIST** dataset available through TensorFlow/Keras.

The dataset contains grayscale images of fashion products.

Each image has:

* 28 × 28 pixels
* Grayscale pixel values
* One of 10 predefined product categories

The dataset is downloaded automatically when the notebook is executed.

---

## Model Architecture

A simple neural network is created using TensorFlow/Keras.

```text
Input Image
     ↓
Flatten Layer
     ↓
Dense Hidden Layer
     ↓
Output Layer
     ↓
Product Category
```

### Model Components

| Component | Purpose                                                 |
| --------- | ------------------------------------------------------- |
| Flatten   | Converts the 28 × 28 image into a suitable input format |
| Dense(64) | Hidden layer that learns patterns from the images       |
| ReLU      | Activation function used in the hidden layer            |
| Dense(10) | Produces an output for each product category            |
| Softmax   | Converts outputs into category probabilities            |

---

## Data Preparation

The original pixel values range from **0 to 255**.

The practical normalizes them to values between **0 and 1**.

```text
Original Pixel Values
0 – 255

        ↓ Normalization

Normalized Pixel Values
0 – 1
```

This makes the data easier for the neural network to process.

---

## Model Training

The neural network is trained using labelled fashion images.

The practical uses:

* **3 epochs**
* **10% validation split**
* **Adam optimizer**
* **Sparse categorical cross-entropy**
* **Accuracy as the evaluation metric**

An epoch means the model has processed the training dataset once.

---

## Model Evaluation

After training, the model is tested using images that were not used during training.

The notebook displays the test accuracy:

```text
Test Accuracy: XX.XX %
```

The exact accuracy may vary slightly.

For example, an accuracy of 87% means that approximately 87 out of 100 test images were classified correctly.

### Important Business Considerations

Accuracy alone may not be enough for real-world deployment.

A company should also consider:

* Cost of incorrect classifications
* Customer experience
* Quality of training data
* Human review
* Impact of incorrect product categories

---

## Predictions

The trained model can predict the category of an unseen product image.

The prediction is compared with the actual category:

```text
Predicted Product
       vs.
Actual Product
```

Students can change the image number and test different products.

---

## Business Application

### Manual Process

```text
Product Image
      ↓
Employee identifies product
      ↓
Employee selects category
      ↓
Product is listed
```

### AI-Assisted Process

```text
Product Image
      ↓
Deep Learning Model
      ↓
Predicted Category
      ↓
Employee Review
      ↓
Product Listing
```

### Possible Business Benefits

An e-commerce company could use image classification to:

* Speed up product listing
* Reduce repetitive manual work
* Improve consistency in product categorization
* Support product search
* Process large numbers of product images
* Assist employees with routine classification

---

## Limitations

The model may make incorrect predictions.

Possible reasons include:

* Similar-looking products
* Limited visual information
* Differences between training and real-world images
* Limitations of the model
* Quality and quantity of training data

Incorrect classifications could affect product listings, search results, recommendations, and customer experience.

Human review can therefore remain important, especially when the model is uncertain or the consequences of an error are significant.

---

## Student Activities

Students are expected to:

1. Identify the input to the Deep Learning model.
2. Identify the output produced by the model.
3. Explain the role of the hidden layer.
4. Identify the activation function used.
5. Record the test accuracy.
6. Find one correctly classified image.
7. Find one incorrectly classified image.
8. Explain the possible business impact of an incorrect prediction.
9. Identify where human review could be used.
10. Suggest another business problem where image classification could be useful.

---

## Key Concepts

### Deep Learning

Deep Learning uses neural networks to learn patterns from data.

### Neural Network

A neural network consists of interconnected layers that transform input data into predictions.

### Training

Training allows the model to learn patterns from labelled examples.

### Testing

Testing evaluates the model using previously unseen data.

### Classification

Classification assigns an input to one of several predefined categories.

### Prediction

Prediction is the category selected by the trained model for a new image.

---

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* Google Colab
* Fashion MNIST

---

## Repository Structure

```text
part-a/
└── deep-learning/
    ├── Deep_Learning_Fashion_Classification_Name.ipynb
    ├── README.md
    └── prediction-screenshot.png
```

---

## How to Run

1. Open the notebook in Google Colab.
2. Run the cells from top to bottom.
3. Allow the Fashion MNIST dataset to download.
4. View the sample fashion images.
5. Train the neural network.
6. Check the test accuracy.
7. Test different image numbers.
8. Find a correct prediction.
9. Find an incorrect prediction.
10. Take a screenshot showing the product image, predicted category, and actual category.
11. Add the screenshot to the repository.

---

## Submission

Rename the notebook:

```text
Deep_Learning_Fashion_Classification_Name.ipynb
```

Upload the notebook and screenshot to:

```text
part-a/deep-learning/
```

### Required Screenshot

The screenshot should show:

* Product image
* Predicted category
* Actual category

---

## Final Reflection

The practical demonstrates how a Deep Learning model can convert image data into useful business information.

An e-commerce company could use such a system to assist with product categorization and reduce repetitive manual work. However, model accuracy, data quality, business risks, and human oversight should be considered before deploying an AI system in a real business environment.

---

## Key Takeaways

* Deep Learning can learn patterns from images.
* Neural networks contain input, hidden, and output stages.
* Training uses historical labelled examples.
* Testing evaluates performance on unseen examples.
* Image classification assigns products to predefined categories.
* Model predictions are not always correct.
* AI can assist employees with repetitive classification tasks.
* Human oversight can remain important in business applications.
