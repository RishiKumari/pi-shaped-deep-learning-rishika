# pi-shaped-deep-learning-rishika
day1-neural-networks-workshop

#**Core Concept Questions & Answers**

1. What is the role of feature scaling/normalization in training neural networks?
-Feature scaling ensures that all input features are on a similar scale. This helps the network train faster, prevents some features from dominating, and improves convergence.

2. Why do we split data into training and testing sets?
-To evaluate how well the trained model generalizes to unseen data.
  Training set is for fitting the model, test set is for unbiased performance evaluation.

3. What is the purpose of activation functions like ReLU or Sigmoid?

  -ReLU (Rectified Linear Unit): Introduces non-linearity, helps avoid vanishing gradients, and speeds up training.
  -Sigmoid: Outputs values between 0 and 1, making it useful for probability-based binary classification.
   Activation functions allow neural networks to model complex, non-linear relationships.

4. Why is binary cross-entropy commonly used as a loss function for classification?
 - Binary cross-entropy measures the difference between predicted probabilities and actual class labels. It penalizes
   incorrect predictions more strongly and is mathematically aligned with maximizing likelihood in binary classification tasks.

5. How does the optimizer (e.g., Adam) affect training compared to plain gradient descent?
 - Adam is an adaptive optimizer that adjusts the learning rate for each parameter based on past gradients. Compared to plain gradient descent,
   it converges faster, handles sparse gradients better, and usually requires less tuning.

6. What does the confusion matrix tell you beyond just accuracy?
  -It shows counts of TP, TN, FP, FN. This reveals specific errors (e.g., misclassifying positives as negatives), which accuracy alone might hide.

7. How can increasing the number of hidden layers or neurons impact model performance?

  -Can improve the ability to learn complex data patterns.
  -But may lead to overfitting, higher computation cost, and harder optimization if excessive.

8. What are some signs that your model is overfitting the training data?

-Very high training accuracy but low test accuracy.
-Training loss keeps dropping while validation loss rises.
-Model memorizes instead of generalizing.

9. Why do we evaluate using precision, recall, and F1-score instead of accuracy alone?
 Accuracy can be misleading in imbalanced datasets.

 -Precision: Proportion of predicted positives that are correct.
 -Recall: Proportion of actual positives detected.
 -F1-score: Balances precision and recall.
These give a more complete view of performance.

10. How would you improve the model if it performs poorly on the test set?

-Gather more data.
-Use regularization (dropout, L2).
-Tune hyperparameters (learning rate, epochs, layers).
-Apply early stopping.
-Try feature engineering or data augmentation.
