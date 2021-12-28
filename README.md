# Deep Learning Classification of Stanford Cars Dataset

Used convolutional neural networks (CNNs) to classify car images from the Stanford Cars Dataset.  

## Preprocessing: 
- Normalize image sizes to 224x224
- Min-Max scaling
- Data Augmentation (rotations, zooms, flips, shifts, etc.)
- Cropped image to minimize backgoround noise in samples

## CNN Models:
### 1. CNN control model: 
- Four convolutional layer
- Dropout layer after each set of two convolutional layers
- One max pooling layer
- Convolutional layers are followed by Relu activation
- Softmax convolutional layer used at the end of the classification

### 2. Alexnet:
- Five convolutional layers followed by, 
- Three fully connected layers
- Convolutional layers are followed by Relu non-linear activation layers
- Layers 1, 3, 5 are followed by batch normalization layer and a 3x3 max pooling layer that performs overlap pooling
- Three fully connected layers used at the end of the model for classification

### 3. VGG-16 Architecture with Transfer Learning 
- 16 layers in total 
- 13 convolutional layers with a 3x3 filter, followed by 3 fully-connected layers 
- Convolutional layers are grouped into batches of 2-3 layers, and a 2x2 max pooling layer is placed between each batch
- Fully connected layers are featured at the end of the model to classify the image
- VGG-16 model weights are pre-trained on the ImageNet dataset for transfer learning 

### 4. ResNet50 Architecture with Transfer Learning (Deep residual network similar to CNN)
- ResNet50 architecture comprises four stages
- 1st Stage: Convolutional layer of 7x7 kernel then a max-pooling layer of 3x3 kernel.  Followed by three residual blocks with each block performing a convolutional operation on three layers.  The three residual blocks alternate kernels of 1x1 and 3x3. Blocks are residual because they have identity connection from the start to the end of the block.  
- 2nd Stage & 3rd Stage: Replicate stage one, but the channel width is doubled and half the input size 
- 4th Stage: Flatten layer with a fully connected dense layer to converge neurons into our 49 classes

## Data was adapted from the following Kaggle links:

- Raw dataset developed and released by Stanford: https://www.kaggle.com/jessicali9530/stanford-cars-dataset

- Classes in dataset organized into separate folders: https://www.kaggle.com/jutrera/stanford-car-dataset-by-classes-folder

- Classes in dataset organized into separate folders, and each image cropped around its bounding-box: https://www.kaggle.com/sungtheillest/vehicledetected-stanford-cars-data-classes-folder

