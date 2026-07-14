# AI vs Real Image Classifier

---

## Table of Contents
1. [Repository Contents](#repository-contents)
2. [Task Overview](#task-overview)
3. [Model Training Steps (Teachable Machine)](#model-training-steps-teachable-machine)
4. [Prerequisites & Setup in Google Colab](#prerequisites--setup-in-google-colab)
5. [Code Implementation & Modifications](#code-implementation--modifications)
6. [How to Run](#how-to-run)
7. [Expected Results](#expected-results)

---

## Repository Contents
* **`image_recognition_model.ipynb`** – The Google Colab notebook containing the modified starter code to display the input image and its class.
* **`keras_model.h5`** – The trained deep learning model weights exported from Teachable Machine.
* **`labels.txt`** – The text file containing the target categories (`0 Real_Images` and `1 AI_Generated_Images`).
* **`README.md`** – Main documentation file explaining the project steps and execution.

---

## Task Overview
This project was developed as part of the **Smart Methods Training Program (July 2026)**. 

The primary objective is to train an image classification model using Google's Teachable Machine to distinguish between **Real** and **AI-Generated** images. After downloading the pre-trained weights (`.h5`), the starter code provided by the platform was run and tested locally inside **Google Colab**, with custom modifications using `matplotlib` to visually display the actual input image alongside its predicted class and confidence score.

---

## Model Training Steps (Teachable Machine)

1. **Initialize Project:** Opened Teachable Machine, clicked *Get Started*, and selected *Image Project* -> *Standard image model*.
2. **Define Classes:** Created two distinct classes based on the task requirements:
   * **Class 1:** `Real_Images`
   * **Class 2:** `AI_Generated_Images`
3. **Upload Training Data:** Uploaded a dataset of authentic photos into the Real class, and AI-generated graphics into the AI class.
4. **Train Model:** Clicked *Train Model* to let the system learn the distinctive features and patterns of each category.
5. **Export the Model:** Clicked *Export Model*, selected **TensorFlow** -> **Keras**, and downloaded `keras_model.h5` along with `labels.txt`. Copy-pasted the provided starter code template.

---
<img width="941" height="482" alt="Screenshot 2026-07-09 192703" src="https://github.com/user-attachments/assets/fda7be36-b19c-4f0b-8d3e-7beb4cfe565e" />


---
## Prerequisites & Setup in Google Colab

Before running the code, you must upload the necessary files to your Google Colab session:

1. Open **Google Colab** and create a *New Notebook*.
2. Click the **Files icon** (folder icon) on the left-hand sidebar.
3. Click the **Upload to session storage** button.
4. Select and upload `keras_model.h5`, `labels.txt`, and the picture you want to test the model with (e.g., `titanic.png`).

---

## Code Implementation & Modifications

The standard template code downloaded from Teachable Machine was updated in Colab with custom modifications to enhance the output visualization:

* **Image Display Integration:** Added `matplotlib.pyplot` (`plt.imshow(image)`) to render the actual image being tested right inside the Colab notebook output.
* **Actual Class Printing:** Modified the print logic to cleanly display the exact predicted class name while stripping out indexing numbers (e.g., displaying `Real_Images` instead of `0 Real_Images`).

---

## How to Run

1. Paste the modified Python code into a cell inside your **Google Colab** notebook.
2. Make sure your test image path matches the file name uploaded in the session storage (e.g., `Image.open("titanic.png")`).
3. Click the **Play button** (Run cell) to execute the code and verify the results.

---

## Expected Results

When the script executes successfully inside Google Colab, a window will display the tested image, and the cell output will show the following results:

<img width="276" height="305" alt="Screenshot 2026-07-14 173034" src="https://github.com/user-attachments/assets/504c2e76-a435-493c-9043-666efcfe3fff" />

