# Day 4 — Model Optimization Techniques (Fashion-MNIST)

Objective: Improve a baseline CNN using hyperparameter tuning and compression techniques, then prepare a deployment-ready TFLite model. We compare baseline vs optimized models by accuracy, model size and inference speed.

Steps:
1. Load & preprocess data
2. Build a baseline CNN, train and record accuracy + time
3. Hyperparameter experiments (2 configs) — compare results
4. Model compression: Dropout + TensorFlow model pruning
5. Convert best model to TFLite and compare sizes + inference speed
6. Evaluate: accuracy, loss curves, confusion matrix


## Core Concept Questions & Answers
# 1. Why is hyperparameter tuning important, and what trade-offs does it involve?

Hyperparameter tuning is important because it directly affects a model’s accuracy, speed, and generalization ability. The trade-off is often time vs. performance: better results usually require more compute, experimentation, and training cycles.

# 2. How does model pruning or compression impact performance and resource usage?

Pruning or compression reduces model size and speeds up inference by removing unnecessary parameters. However, it can slightly reduce accuracy if over-applied, so the challenge is balancing efficiency with predictive performance.

# 3. Why is dropout effective in preventing overfitting?

Dropout randomly deactivates a fraction of neurons during training, forcing the network to learn more robust representations. This prevents over-reliance on specific nodes and reduces overfitting.

# 4. What challenges arise when deploying deep learning models in production?

Key challenges include:

Large model size and slow inference

Limited hardware (edge/mobile devices)

Maintaining accuracy after optimization

Handling continuous retraining and monitoring in real-world environments

# 5. How does TensorFlow Lite (or ONNX, TorchScript) help in deployment optimization?

These frameworks convert large models into lightweight, platform-optimized versions. They reduce size, speed up inference, and make deployment feasible on mobile devices, IoT systems, and edge hardware.

# 6. What is the balance between model accuracy and efficiency in real-world applications?

In practice, we rarely chase maximum accuracy at all costs. Instead, we aim for a balance where the model is accurate enough while being fast, lightweight, and cost-efficient for deployment.

# 7. How can hardware (GPU, TPU, Edge devices) influence optimization strategies?

Hardware dictates optimization strategies:

GPUs/TPUs favor parallelization and large models.

Edge devices require lightweight, pruned, or quantized models.

Specialized hardware (like NPUs in smartphones) encourages deployment-friendly frameworks like TFLite.

# 8. Looking ahead, how might optimization differ for Transformer-based models compared to CNNs/RNNs?

Transformers are larger and more compute-intensive, so optimization often focuses on:

Knowledge distillation

Low-rank approximations

Sparse attention mechanisms

Quantization & pruning at scale

In contrast, CNN/RNN optimizations are usually lighter and more focused on reducing parameter redundancy.
