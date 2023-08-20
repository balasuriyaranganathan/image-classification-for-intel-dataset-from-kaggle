<h1>IMAGE CLASSIFICATION FOR INTEL DATASET FROM KAGGLE</h1>
<p>This repository contains a python script for training a Convolutional Neural Network CNN model for image classification using Tensorflow and Keras</p>

<h2>Setup</h2>
1. Install the following libraries


```bash
pip install tensorflow
```

```bash
pip install numpy
```

```bash
pip install scikit-learn
```
```bash
pip install pillow
```
<ul>
<li>2. Create a dev cloud account in Intel dev cloud jupyter hub</li>
<li>3. Clone this repository in the linux terminal in dev cloud</li>
<li>4. Download the dataset from kaggle https://www.kaggle.com/datasets/puneet6060/intel-image-classification</li>
<li>5. Compile the code in intel dev cloud for faster compilation and better results</li>
</ul>
<h2>Usage</h2>
1. Open the .ipynb file in dev cloud.
2. run the cell in the given order.
3. Change the training_dir to the dataset

## Model Architecture

The Convolutional Neural Network (CNN) model architecture is designed to extract features from input images and classify them into different categories. Here's an overview of the layers used in the model:

<table>
  <tr>
    <th>Layer Type</th>
    <th>Configuration</th>
    <th>Output Shape</th>
  </tr>
  <tr>
    <td>Input</td>
    <td>Conv2D<br>Filters: 32<br>Kernel Size: (3, 3)<br>Activation: ReLU</td>
    <td>(150, 150, 32)</td>
  </tr>
  <tr>
    <td>Max Pooling</td>
    <td>Pool Size: (2, 2)</td>
    <td>(75, 75, 32)</td>
  </tr>
  <tr>
    <td>Convolutional</td>
    <td>Conv2D<br>Filters: 64<br>Kernel Size: (3, 3)<br>Activation: ReLU</td>
    <td>(73, 73, 64)</td>
  </tr>
  <tr>
    <td>Max Pooling</td>
    <td>Pool Size: (2, 2)</td>
    <td>(36, 36, 64)</td>
  </tr>
  <tr>
    <td>Convolutional</td>
    <td>Conv2D<br>Filters: 128<br>Kernel Size: (3, 3)<br>Activation: ReLU</td>
    <td>(34, 34, 128)</td>
  </tr>
  <tr>
    <td>Max Pooling</td>
    <td>Pool Size: (2, 2)</td>
    <td>(17, 17, 128)</td>
  </tr>
  <tr>
    <td>Flatten</td>
    <td>-</td>
    <td>(36992,)</td>
  </tr>
  <tr>
    <td>Fully Connected</td>
    <td>Dense<br>Neurons: 128<br>Activation: ReLU</td>
    <td>(128,)</td>
  </tr>
  <tr>
    <td>Output</td>
    <td>Dense<br>Neurons: 6 (Number of classes)<br>Activation: Softmax</td>
    <td>(6,)</td>
  </tr>
</table>

The model starts with convolutional layers that extract features from the images, followed by max pooling layers to downsample the data. After flattening the output, fully connected layers perform classification. The output layer uses the softmax activation function for class probabilities.
<h2>
  evaluation metrics
</h2>

The model's performance is evaluated using the following metrics:

<table>
  <tr>
    <th>Metric</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Loss</td>
    <td>The loss is a measure of the model's prediction error during training and evaluation. Lower values indicate better predictions.</td>
  </tr>
  <tr>
    <td>Accuracy</td>
    <td>The accuracy represents the percentage of correctly classified images in the validation set. It measures the overall correctness of the model's predictions.</td>
  </tr>
</table>

During training, the model's progress is monitored using these metrics to ensure that it is learning and improving over epochs.

  
