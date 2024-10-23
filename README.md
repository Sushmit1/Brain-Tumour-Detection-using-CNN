## Brain-Tumour-Detection-using-CNN

This project utilizes a Convolutional Neural Network (CNN) to detect brain tumors from MRI images. The model is trained on a dataset of MRI scans categorized as "tumorous" or "non-tumorous" and applies various preprocessing steps, including cropping and normalization, to enhance the learning process. The model achieves an Test Accuracy of 88% and F1-Score of 90%.

### 1. About the Dataset : 
The dataset contains brain MRI images categorized into two classes:
* Yes: Tumorous MRI scans (155 images)
* No: Non-tumorous MRI scans (98 images)

* #### Data Augmentation : 

The dataset contains 2 folders: yes and no, which hold 253 Brain MRI images. The yes folder contains 155 MRI images of tumorous brains, while the no folder contains 98 MRI images of non-tumorous brains. Since the dataset is small and imbalanced (61% tumorous and 39% non-tumorous), data augmentation was used to generate additional images, which not only increased the dataset size but also helped to balance the two classes. Data augmentation techniques were applied to generate synthetic images by performing transformations like rotations, flips, brightness adjustments, and more. 
Augmentation Techniques:
The following augmentation techniques were used:

* Rotation (up to 10 degrees)
* Width and height shifts (up to 10%)
* Shear transformations
* Brightness adjustments (between 30% and 100%)
* Horizontal and vertical flips
* Filling missing parts using nearest pixels

Summary of Augmented Data:
* Total examples after augmentation: 2064 images
* Percentage of tumorous examples: 52.57% (1085 images)
* Percentage of non-tumorous examples: 47.43% (979 images)
This augmented dataset is now ready to be used for training a convolutional neural network (CNN).

### 2. Installation : 
To run this project, you'll need to install the following dependencies:

pip install tensorflow
pip install opencv-python
pip install imutils
pip install numpy
pip install matplotlib
pip install scikit-learn

### 3. Data Preparation and Preprocessing
The dataset images are preprocessed with the following steps:
* Cropping: Extract the brain region from the MRI scan by identifying extreme points in the image. This reduces unnecessary information.
* Resizing: All images are resized to a uniform dimension of 240x240 pixels.
* Normalization: The pixel values are normalized to fall within the range 0-1

### 4. Model Architecture
The CNN model is constructed using TensorFlow and consists of several layers:
* Convolutional layers: Extract features from input images using filters.
* Batch Normalization: Normalizes the output of the convolutional layers to improve training speed and stability.
* Max Pooling: Reduces the spatial dimensions of the output.
* Dense layers: Fully connected layers for classification.

### 5. Training and Evaluation
The model is compiled with the binary cross-entropy loss function and optimized using the Adam optimizer. It is evaluated on F1 Score for balanced performance on both classes.
Training can be monitored through TensorBoard for loss and accuracy visualization.

### 6. Results
After training, the model achieves the following results on the test set:

Validation Accuracy: 88%
Test Accuracy: 88%
Validation F1 Score: 89%
Test F1 Score : 90%
