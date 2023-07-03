# Satellite-Image-Segmentation

This project focuses on satellite image segmentation using deep learning techniques. The goal is to accurately classify and segment different objects and regions within satellite imagery, enabling various applications such as land cover mapping, urban planning, and environmental monitoring.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Data](#data)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction

In this project, we utilize the power of deep learning to perform pixel-wise semantic segmentation on satellite imagery. The segmentation models are trained to accurately classify each pixel into predefined classes, enabling the identification and delineation of different objects and land cover types within the images.

## Features

- Implementation of Simple UNet and Multi-UNet models for satellite image segmentation.
- Data preprocessing techniques to prepare the satellite imagery and corresponding masks.
- Training process with configurable hyperparameters and callbacks.
- Evaluation and visualization of training and validation performance.
- Comparison of model performance and analysis of results.

## Installation

1. Clone the repository: `git clone https://github.com/your_username/satellite-image-segmentation.git`
2. Navigate to the project directory: `cd satellite-image-segmentation`
3. Install the required dependencies: `pip install -r requirements.txt`

## Usage

1. Prepare the dataset by organizing the satellite imagery and corresponding masks in separate directories.
2. Adjust the configuration parameters in the code according to your dataset and training requirements.
3. Run the training script: `python train.py`
4. Monitor the training progress and evaluate the model's performance.
5. Use the trained model for segmenting new satellite images or further fine-tuning.

## Data

The dataset used for this project consists of satellite imagery and corresponding ground truth masks. It should be organized as follows:

```
dataset/
    ├── train_images/
    │   ├── image_1.jpg
    │   ├── image_2.jpg
    │   └── ...
    └── train_masks/
        ├── mask_1.png
        ├── mask_2.png
        └── ...
```

Ensure that the images and masks have the same filenames and are aligned correctly.

## Model Architecture

Two models were implemented for satellite image segmentation:

1. Simple UNet: A basic UNet architecture consisting of an encoder and a decoder with skip connections. This model provides a good baseline for the task.

2. Multi-UNet: An extended version of the Simple UNet model with additional layers and parameters to capture more complex features and improve segmentation performance.

## Training

To train the models, run the training script `train.py` with appropriate configuration settings. Adjust the hyperparameters, such as learning rate and batch size, to optimize the training process. The models will be saved periodically during training for future use.

## Results

The trained models' performance was evaluated on the validation dataset, measuring accuracy and loss. The results showed that:

- Simple UNet achieved a training accuracy of 77.15% and a validation accuracy of 70.42% after 50 epochs.

- Multi-UNet achieved a higher training accuracy of 80.61% but had a slightly lower validation accuracy of 74.06% after 31 epochs.

Further analysis is needed to understand the validation performance difference and potential improvements for both models.

## Contributing

Contributions to this project are welcome. If you find any issues or have suggestions for improvements

, please feel free to submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

Feel free to customize the content as per your project's specific details and requirements.
