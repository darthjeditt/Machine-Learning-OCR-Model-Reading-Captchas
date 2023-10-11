# OCR Model for Reading Captchas

This project focuses on training an OCR (Optical Character Recognition) model to read captchas. The goal is to develop a model that can accurately recognize the characters present in captcha images.

## Setup and Dependencies
To run the project, ensure you have the following dependencies installed:
- TensorFlow
- Keras
- NumPy
- Matplotlib

You can install the dependencies by running the following command:
```
pip install tensorflow keras numpy matplotlib
```

## Project Overview
1. Import Libraries: Import the necessary libraries, including TensorFlow, Keras, NumPy, and Matplotlib, to perform the required tasks.

2. Download the Dataset: Download the captcha dataset from the provided URL using the `requests` library. The dataset contains captcha images in PNG format.

3. Path to the Data Directory: Specify the path to the data directory and extract the downloaded zip file.

4. Preprocessing: Preprocess the dataset by getting the list of image paths and corresponding labels. Find the unique characters present in the labels.

5. Split Data: Implement a function to split the data into training and validation sets based on a given train size. Shuffle the data if required.

6. Encode Single Sample: Define a function to encode a single sample by reading the image file, decoding it, resizing it, and converting it to a floating-point tensor. Also, convert the label to a numeric representation.

7. Create Datasets: Create dataset objects for the training and validation data. Apply the `encode_single_sample` function to preprocess the data, batch the datasets, and prefetch the data for efficient processing.

8. Visualize the Data: Display a grid of captcha images with their corresponding labels to visualize the data.

9. Build the Model: Define a custom CTC (Connectionist Temporal Classification) layer and build the OCR model using convolutional and recurrent layers.

10. Training the Model: Train the OCR model using the training dataset and evaluate it on the validation dataset. Use the `EarlyStopping` callback to stop training early if the validation loss does not improve.

11. Inference: Use the trained model to make predictions on a batch of validation samples. Decode the predictions to get the recognized text and compare it with the original labels. Display the captcha images with their predicted and original labels.

## Usage
1. Clone or download the project.
2. Install the project dependencies as mentioned in the "Setup and Dependencies" section.
3. Run the Python script or Jupyter Notebook containing the project code.
4. Follow the output to observe the training progress and the model's predictions on the validation data.

## Conclusion
The "OCR Model for Reading Captchas" project demonstrates the training of an OCR model to recognize characters in captcha images. By preprocessing the dataset, building the model, and training it on the data, we can achieve accurate recognition of the captcha text. The trained model can be used for various applications involving captcha recognition and text extraction from images.

## Contributing
I would love your help! Contribute by forking the repo and opening pull requests. Please ensure that your code passes the existing tests and linting, and write tests to test your changes if applicable.

All pull requests should be submitted to the main branch.
