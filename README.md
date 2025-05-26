#Digit Recognizer Project (Kaggle)

This project demonstrates how to use Artificial Neural Networks (ANN) and Convolutional Neural Networks (CNN) to recognize handwritten digits (0–9) using the [Digit Recognizer](https://www.kaggle.com/competitions/digit-recognizer) competition on Kaggle.

---

##Project Structure

```
Digit_Recognizer_attempt_1.ipynb   # Main notebook with ANN and CNN models
README.md                          # Project overview and usage guide
```

---

## Dataset Overview

* **Train Set:** 42,000+ grayscale images, 28x28 pixels each
* **Test Set:** Similar images without labels
* **Pixel Values:** Range from 0 (white) to 255 (black)
* **Goal:** Predict digit labels for the test set

---

## What This Project Covers

### Data Preprocessing

* Verified no missing values
* Normalized pixel values (0–255 → 0–1)
* Converted training data to NumPy arrays and split into training/testing sets

### Artificial Neural Network (ANN)

* **Architecture:** 3–4 hidden layers with `ReLU` and `softmax` output
* **Loss Function:** `sparse_categorical_crossentropy`
* **Optimizer:** Adam
* **Regularization:** Dropout + Batch Normalization + EarlyStopping
* **Evaluation:** Accuracy and Confusion Matrix

###Convolutional Neural Network (CNN)

* **Architecture:**

  * Conv2D → MaxPooling → Conv2D → MaxPooling → Flatten → Dense
* **Activation:** ReLU and softmax
* **Performance:** Accuracy improved slightly from ANN baseline

---

## 📈 Results

| Model                                  | Accuracy |
| -------------------------------------- | -------- |
| ANN (Basic)                            | 97.99%   |
| ANN (with dropout, batch norm, tuning) | 95.92% |
| CNN (2 Conv layers + 2 dense)          | 99.01%   |

---

## ⚙️ Requirements

```bash
pip install numpy pandas matplotlib seaborn tensorflow scikit-learn
```

---

## How to Run

1. Clone the repository
2. Open `Digit_Recognizer_attempt_1.ipynb` in Jupyter Notebook / Colab / Kaggle
3. Run each cell step-by-step to:

   * Explore the data
   * Train the ANN
   * Train the CNN
   * Evaluate and visualize model performance

---

## Notes

* Models were evaluated only on the provided train/test Kaggle splits.
* No external data or augmentation was used.

---

## Contact

Built by Stephen Philip | 📧 [stephenphilip28@gmail.com](mailto:stephenphilip28@gmail.com)
