CS5720 Neural network and Deep learning,

CRN:-23848

Name:- Narina Lakshmi Durga.

student ID:-700757569.

Home Assignment 1.

Q1.Tensor Manipulations & Reshaping

The code demonstrates creating a random tensor, reshaping and transposing it, and performing broadcasting during element-wise addition with another tensor. It shows how to manipulate tensor shapes and dimensions in TensorFlow, including reshaping from (4, 6) to (2, 3, 4), transposing it to (3, 2, 4), and broadcasting a smaller tensor for arithmetic operations.

Q2.Loss Functions & Hyperparameter Tuning

The code calculates and visualizes the loss for a multi-class classification problem using Sparse Categorical Crossentropy (CCE). It computes the loss between true class labels and predicted probabilities, then plots the loss value. The loss function is used without logits (from_logits=False) since the predictions are probabilities, not raw scores.

Q3.rain a Model with Different Optimizers

This code compares two different optimizers, Adam and SGD, for training a neural network on the MNIST dataset, which consists of images of handwritten digits. The dataset is first loaded and normalized so that the pixel values range between 0 and 1. A simple neural network is defined with a Flatten layer to reshape the images, a Dense layer with 128 neurons and ReLU activation, a Dropout layer to reduce overfitting, and an output Dense layer with 10 neurons and softmax activation for multi-class classification.

Two separate models are created and trained using the Adam and SGD optimizers. Both models are compiled with the same loss function, sparse categorical crossentropy, and evaluated using accuracy. They are trained for 10 epochs with validation data from the test set. The training and validation accuracy of both models are plotted to compare their performance over the epochs.

The resulting plots show how the training accuracy increases and how well each optimizer generalizes to the test set. Finally, the final training and validation accuracy values are printed for both models, allowing for a direct comparison of their performance. This experiment demonstrates the differences in convergence speed and generalization ability between Adam and SGD optimizers for multi-class classification tasks.

Q4.Train a Neural Network and Log to TensorBoard

This script trains a simple neural network on the MNIST dataset while using TensorBoard to monitor and visualize the model's performance. TensorBoard allows users to track training and validation accuracy, loss trends, and even view histograms of weights and biases. It is a powerful tool for model debugging and optimization.

4.1. What patterns do you observe in the training and validation accuracy curves?

In general, when you plot training and validation accuracy curves, you might observe the following patterns:

Training Accuracy: This curve typically increases steadily as the model learns from the training data, especially in the earlier epochs. Since the model has access to the training data during training, the training accuracy tends to improve consistently.

Validation Accuracy: The validation accuracy, which is computed on unseen data (the test/validation set), may start lower than training accuracy, but it should gradually improve as the model generalizes to new data. Initially, the gap between training and validation accuracy might be small, but if the model overfits, the validation accuracy could plateau or even decline after a certain number of epochs.

Overfitting Pattern: A clear sign of overfitting would be when the training accuracy continues to improve, but the validation accuracy starts to stagnate or decline. This suggests that the model is memorizing the training data rather than learning general patterns, resulting in poor generalization to unseen data.

 4.2.How can you use TensorBoard to detect overfitting?
 
TensorBoard is a powerful tool for detecting overfitting by visually comparing the following:

Training vs. Validation Accuracy: If the training accuracy is much higher than the validation accuracy and continues to improve while the validation accuracy stagnates or decreases, this could indicate overfitting. Overfitting occurs when the model becomes too complex and learns patterns specific to the training data, rather than generalizing well to new data.

Training vs. Validation Loss: If the training loss decreases continuously but the validation loss starts to increase, this is another strong indicator of overfitting. The model is minimizing error on the training set but failing to generalize well to the test/validation set.

By using TensorBoard, you can visually inspect these curves and determine whether your model is overfitting. If you detect overfitting early, you can take corrective actions such as using dropout, adding regularization, or reducing the model complexity.

4.3.What happens when you increase the number of epochs?
Increasing the number of epochs has the following potential effects:

Improved Performance (up to a point): Initially, increasing the number of epochs allows the model to learn more from the data, leading to improved accuracy on both the training and validation sets. The model has more opportunities to adjust its weights, reducing both training and validation loss.

Risk of Overfitting: After a certain point, continuing to increase the number of epochs can lead to overfitting. As the model learns more from the training data, it may start to memorize specific details and noise, rather than generalizing well to unseen data. This is where the validation accuracy may plateau or decline, even though training accuracy continues to increase.

Stagnation: After a certain number of epochs, the model may reach a plateau where further epochs don’t yield significant improvement in performance. This could indicate that the model has learned as much as it can from the data, and additional training may not help.
