## Objective: Build and train a Convolutional Neural Network (CNN) on the Fashion-MNIST dataset. Evaluate the trained model’s performance using classification metrics. 

### Task Flow: 
1. Load the Fashion-MNIST dataset (train + test sets).
2. Preprocess the data:
   - Normalize pixel values to [0,1]
   - Reshape input images to (28,28,1)
   - One-hot encode labels
3. Build a Convolutional Neural Network (CNN):
   - Convolution + MaxPooling layers
   - Fully connected layers with softmax output
4. Compile and train the model on training data.
5. Evaluate on test set using accuracy and confusion matrix.
6. Visualize results with confusion matrix and accuracy curves.


## Core Concept Questions
### 1. What advantages do CNNs have over traditional fully connected neural networks for image data?

CNNs capture spatial patterns (edges, shapes, textures) using local filters, reducing the number of parameters compared to fully connected layers. This makes them more efficient and effective for image recognition.

### 2. What is the role of convolutional filters/kernels in a CNN?

Filters (kernels) slide over the image, performing multiplication and summation, to extract important features such as edges, corners, or textures that represent patterns in the data.

### 3. Why do we use pooling layers, and what is the difference between MaxPooling and AveragePooling?

Pooling reduces the spatial size of feature maps, making computation faster and preventing overfitting.

MaxPooling: takes the maximum value (captures strongest features).

AveragePooling: takes the average value (captures overall smoothness).

### 4. Why is normalization of image pixels important before training?

Normalization (scaling pixels to [0,1]) ensures stable training by keeping values small, improving convergence, and preventing exploding gradients.

### 5. How does the softmax activation function work in multi-class classification?

Softmax converts raw scores (logits) into probabilities for each class, ensuring all probabilities sum to 1, and the class with the highest probability is chosen as output.

### 6. What strategies can help prevent overfitting in CNNs?

Dropout: randomly disabling neurons during training.

Data Augmentation: creating variations of training data (rotation, flip, zoom).

Regularization (L2): adding penalty to large weights.

Early Stopping: stopping when validation performance no longer improves.

### 7. What does the confusion matrix tell you about model performance?

The confusion matrix shows how many predictions are correct or misclassified across all classes, helping identify which categories the model struggles with.

### 8. If you wanted to improve the CNN, what architectural or data changes would you try?

Adding more convolutional/pooling layers.

Using Batch Normalization for stability.

Trying advanced architectures (ResNet, VGG).

Increasing training data or applying stronger augmentation.

Tuning hyperparameters like learning rate, optimizer, or batch size.
