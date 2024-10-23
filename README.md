## Brain-Tumour-Detection-using-CNN

This project utilizes a Convolutional Neural Network (CNN) to detect brain tumors from MRI images. The model is trained on a dataset of MRI scans categorized as "tumorous" or "non-tumorous" and applies various preprocessing steps, including cropping and normalization, to enhance the learning process.

* ### About the Dataset : 
The dataset contains brain MRI images categorized into two classes:
* Yes: Tumorous MRI scans (155 images)
* No: Non-tumorous MRI scans (98 images)

### Installation : 
To run this project, you'll need to install the following dependencies:

pip install tensorflow
pip install opencv-python
pip install imutils
pip install numpy
pip install matplotlib
pip install scikit-learn

### Data Preparation and Preprocessing
The dataset images are preprocessed with the following steps:
* Cropping: Extract the brain region from the MRI scan by identifying extreme points in the image. This reduces unnecessary information.
* Resizing: All images are resized to a uniform dimension of 240x240 pixels.
* Normalization: The pixel values are normalized to fall within the range 0-1

### Model Architecture
The CNN model is constructed using TensorFlow and consists of several layers:
* Convolutional layers: Extract features from input images using filters.
* Batch Normalization: Normalizes the output of the convolutional layers to improve training speed and stability.
* Max Pooling: Reduces the spatial dimensions of the output.
* Dense layers: Fully connected layers for classification.

### Training and Evaluation
The model is compiled with the binary cross-entropy loss function and optimized using the Adam optimizer. It is evaluated on F1 Score for balanced performance on both classes.
Training can be monitored through TensorBoard for loss and accuracy visualization.

### Results
After training, the model achieves the following results on the test set:

Validation Accuracy: 88%
Test Accuracy: 88%
Validation F1 Score: 89%
Test F1 Score : 90%
