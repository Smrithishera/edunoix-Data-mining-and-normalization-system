This is a part of my Edegree Course from Edunoix

Explanation:
Load and Normalize Data:

The MNIST dataset is loaded and reshaped to include a channel dimension (28x28 images, 1 channel for grayscale).
Image data is normalized to the range [0, 1] for better performance.
Labels are converted to integers.
Model Architecture:

Conv2D Layers: The first layer has 32 units and a 3x3 kernel, with relu activation. The second Conv2D layer has 64 units and relu activation.
MaxPooling2D Layer: Pooling is applied with a 2x2 pooling size to reduce spatial dimensions.
Dense Layers: After flattening the convolutional output, we add a fully connected (Dense) layer with 128 units (relu) and an output layer with 10 units (softmax for classification).
Compile and Train:

The model is compiled using Adam optimizer, sparse categorical crossentropy (since labels are integers), and accuracy as the metric.
The model is trained for 5 epochs on the training data.
Evaluation:

The model is evaluated on the test data, and the output (loss and accuracy) is saved into variables using .evaluate().
