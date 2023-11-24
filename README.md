# MLZoomCamp Week 9 - Bees vs. Wasps Classification

This repository contains code for a simple image classification model that distinguishes between bees and wasps. The model is deployed as an AWS Lambda function using TensorFlow Lite.

## Overview

The code consists of a Python script (`lambda_function.py`) designed to run as an AWS Lambda function. The model used for classification is TensorFlow Lite, and the image data is processed using the PIL library.

## Files

- **lambda_function.py**: The main script containing the AWS Lambda function for image classification.
  
## Usage

### Lambda Function

To use the AWS Lambda function, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/DRPproton/mlzoomcamp-week9.git
   cd mlzoomcamp-week9
   ```

2. Deploy the Lambda function by uploading the ZIP file to AWS Lambda. Make sure to set the environment variable `MODEL_NAME` with the model's filename (default is 'bees-wasps-v2.tflite').

3. Once the Lambda function is deployed, you can invoke it by providing a JSON payload with the image URL:

   ```json
   {
       "url": "https://example.com/path/to/image.jpg"
   }
   ```

4. The Lambda function will return a JSON response with the prediction:

   ```json
   {
       "prediction": 0.75
   }
   ```

   Here, the `prediction` value represents the model's confidence in classifying the image.

## Dependencies

- [tflite_runtime](https://www.tensorflow.org/lite/guide/python): TensorFlow Lite for running the model.
- [PIL](https://pillow.readthedocs.io/en/stable/): Python Imaging Library for image processing.

Make sure to install these dependencies before deploying and running the code.

## Model

The pre-trained model file, 'bees-wasps-v2.tflite', is included in the repository. If you wish to use a different model, set the `MODEL_NAME` environment variable accordingly.

## Author

This code was created by [DRPproton](https://github.com/DRPproton) for the MLZoomCamp Week 9 assignment.

Feel free to explore, modify, and use this code for your own projects. If you encounter any issues or have questions, please create an issue in this repository.
