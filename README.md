# Photo Diary Project

## Overview

The **Photo Diary Project** is an automation pipeline designed to align facial images over time, capturing physical changes in appearance. By utilizing deep learning techniques, the project eliminates the tedious task of manual alignment, producing a time-lapse video of aligned faces.

## Motivation

I wanted to document the physical changes in my face over approximately 24 months. However, manually aligning a set of images taken at irregular intervals was infeasible. This project leverages machine learning to automate the alignment process with precision.

## Features

- **Automated Alignment**: Automatically aligns facial images by detecting and positioning the left and right eyes.
- **Deep Learning Model**: Fine-tuned RegNetY-006, an image classification model, to predict eye coordinates (left eye row, left eye column, right eye row, right eye column).
- **Video Generation**: Produces a seamless time-lapse video of aligned facial images.
- **Comparison with Standard Libraries**: Includes a baseline implementation using a standard face detection library for comparison.

## Dataset

- Collected a set of \~75 hand-labeled images, each annotated with:
  - Left Eye (row, column)
  - Right Eye (row, column)
- Images were resized and normalized for consistent input during training.

## Model Details

- **Architecture**: RegNetY-006
- **Training**: Fine-tuned on the dataset to output four coordinates corresponding to eye positions.
- **Performance**: Achieved a MSE validation loss of **0.017** on the dataset.

## Technologies Used

- **Programming Language**: Python
- **Frameworks**: PyTorch, FastAI
- **Computer Vision**: OpenCV

## How It Works

1. **Data Preparation**: Images are resized, normalized, and prepared for model inference.
2. **Model Inference**: Predicts the positions of the left and right eyes for each image.
3. **Image Alignment**: Aligns images based on the predicted eye positions.
4. **Video Creation**: Combines aligned images into a time-lapse video.

## Results

- **Aligned Video**: A time-lapse video showcasing aligned facial images over time. ([Video](https://youtu.be/mNFFHeYp_8Q?si=IhXYXnstvKW1c0UG))

## Future Improvements

- Add support for detecting and aligning more facial landmarks.
- Explore transfer learning with larger pre-trained models for improved accuracy.

