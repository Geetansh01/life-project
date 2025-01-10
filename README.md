# Photo Diary Project

## Overview

The **Photo Diary Project** is an automation pipeline designed to align facial images over time, capturing physical changes in appearance. By utilizing deep learning techniques, the project eliminates the tedious task of manual alignment, producing a time-lapse video of aligned faces.

## Motivation

I wanted to document the physical changes in my face over approximately 24 months. However, manually aligning a set of images taken at irregular intervals was infeasible. This project leverages machine learning to automate the alignment process.

## Features

- **Automated Alignment**: Automatically aligns facial images by detecting and positioning the left and right eyes.
- **Deep Learning Model**: Fine-tuned RegNetY-006, an image classification model, to predict eye coordinates (left eye row, left eye column, right eye row, right eye column).
- **Video Generation**: Produces a time-lapse type video of aligned facial images.
- **Comparison with Standard Libraries**: Includes a baseline implementation using a standard face detection library for comparison.

## Dataset

- Collected a set of \~75 hand-labeled images of myself (all 3264 x 2448 pixels in dimension), each annotated with:
  - Left Eye (row, column in pixels)
  - Right Eye (row, column in pixels)
- Images were resized and normalized for consistent input during training.
<img src="https://github.com/Geetansh01/photodiary-project/blob/main/DataSetSS.jpg" alt="datasetSS" width="500"/>

## Model Details

- **Architecture**: RegNetY-006
- **Training**: Fine-tuned on the dataset to output four coordinates corresponding to eye positions.
- **Performance**: Achieved a MSE validation loss of **0.017** on the dataset.

## Technologies Used

- **Programming Language**: Python
- **Libraries**: PyTorch, FastAI, OpenCV

## Results

- **Aligned Video**: A time-lapse type video showcasing aligned facial images over time. ([Video](https://youtu.be/mNFFHeYp_8Q?si=IhXYXnstvKW1c0UG))

## Future Improvements

- Explore transfer learning with larger pre-trained models for improved accuracy.

