# Nike vs Adidas Shoe Classifier

This project uses deep learning to look at a picture of a shoe and tell whether it is a **Nike** or an **Adidas**.

I built this to practice image classification with a Convolutional Neural Network (CNN).

---

## What this project does

- Takes a shoe image as input
- Predicts the brand: Nike or Adidas
- Shows how accurate the model is on images it has never seen

---

## Dataset

- Images of Nike and Adidas shoes, split into two folders (one per brand)
- Total images: 140
- Split: [ Test - 40 / Train - 100 ]
- Image size used: [ 120 * 120 ]

---

## How it works

1. **Load the images** from the folders
2. **Resize and scale** them so they are all the same size
3. **Build a CNN model** that learns the patterns in the shoes (shapes, logos, stripes)
4. **Train the model** on the training images
5. **Test the model** on new images and check the accuracy

---

## Tools used

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Jupyter Notebook / Google Colab

---

## Results

- Training accuracy: **97.7%** (after 10 epochs)
- Final training loss: **0.0955**
- Testing accuracy: 98.8
  
### Training progress

The model started at around 50% accuracy, which is basically a random guess between two brands. The loss dropped from 52.4 to 0.09 over 10 epochs, and the accuracy kept climbing to 97.7%.

| Epoch | Accuracy | Loss |
|-------|----------|--------|
| 1     | 52.9%    | 52.44  |
| 5     | 71.3%    | 0.498  |
| 8     | 97.7%    | 0.194  |
| 10    | 97.7%    | 0.096  |

### Sample prediction

I tested the model with a new shoe photo that was not in the dataset. The image is converted to grayscale and resized to the same size used in training before it goes into the model.

<img width="595" height="675" alt="image" src="https://github.com/user-attachments/assets/d5e0e44a-810e-411e-aa04-7fa02621c70c" />




The model gave this output:

    [[0.0055, 0.9945]]

This means the model is about 99.4% sure the shoe belongs to class 1, and only about 0.5% sure about class 0.

## How to run it

1. Clone this repo
