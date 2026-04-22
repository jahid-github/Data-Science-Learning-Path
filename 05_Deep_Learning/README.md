# Phase 5 — Deep Learning

Deep learning uses multi-layer neural networks to learn complex patterns directly from raw data. It powers modern computer vision, NLP, and physical AI systems. **PyTorch is the primary framework** — preferred for research, robotics, and edge AI.

---

## Learning Steps

### 1. Neural Network Fundamentals
- Neurons, layers, activation functions: ReLU, Sigmoid, Softmax, Tanh
- Forward pass, loss functions (Cross-Entropy, MSE), backpropagation
- Optimizers: SGD, Adam, RMSprop — learning rate intuition
- Vanishing and exploding gradients — BatchNorm, gradient clipping

### 2. PyTorch Core
- Tensors, autograd, computational graphs
- Building models with `nn.Module`
- Training loops, DataLoaders, data augmentation
- GPU training (`.cuda()`), model saving/loading (`state_dict`)

### 3. Convolutional Neural Networks (CNNs)
- Convolution, pooling, receptive fields
- Architectures: LeNet → AlexNet → VGG → ResNet → EfficientNet
- Transfer learning: fine-tuning pre-trained models from `torchvision`
- Applications: image classification, feature extraction

### 4. Recurrent Neural Networks (RNNs)
- Sequence modeling: vanilla RNN, LSTM, GRU
- Vanishing gradient in RNNs — why LSTMs solve it
- Applications: time-series, sensor data from robots, text sequences
- Encoder-Decoder, seq2seq architecture

### 5. Regularization & Optimization
- Dropout, weight decay, batch normalization, layer normalization
- Learning rate schedules: cosine decay, warmup, ReduceLROnPlateau
- Mixed precision training (AMP) for GPU efficiency

### 6. Model Deployment & Edge AI
- ONNX: export PyTorch models for cross-platform inference
- TorchScript: production-ready, serialized PyTorch models
- TensorRT: NVIDIA GPU-optimized inference (critical for Jetson in robotics)
- ONNX Runtime: cross-platform model inference
- Benchmarking: latency, throughput, memory profiling

---

## Frameworks & Tools

| Tool | Purpose |
|------|---------|
| **PyTorch** | Primary framework — custom models, edge AI, real-time inference, research |
| **TensorFlow** | Production-grade training and deploying scalable models |
| **Keras** | High-level API on top of TensorFlow — rapid prototyping |
| **torchvision** | Pre-trained vision models, transforms, datasets |
| **torchaudio** | Audio processing and feature extraction for PyTorch |
| **ONNX Runtime** | Cross-platform model inference — export from PyTorch/TF |
| **TensorRT** | NVIDIA GPU-optimized inference engine — used on Jetson for robotics edge AI |
| **OpenVINO** | Intel hardware inference optimization |

---

## PDF Resources

* [Neural Network Basics](./Neural_Networks_Basics.pdf)
* [Convolutional Neural Network](./CNN.pdf)
* [Recurrent Neural Network](./RNN.pdf)
* [Convex and Non-Convex Function / Optimization using Gradient Descent](./Optimization_using_Gradient_Descent.pdf)
* [Calculus for Artificial Intelligence / Backpropagation](./Backpropagation.pdf)
* [Vanishing and Exploding Gradients Problem](./Vanishing_and_Exploding_Gradients_Problem.pdf)
* [Deep Learning From Scratch](./Deep_Learning_From_Scratch.pdf)
* [Deep Learning with PyTorch](./Deep_Learning_with_PyTorch_1.pdf)
* [Keras Cheat Sheet](./Keras_Cheat_Sheet_gssmi8.pdf)

---

## Learning Resources

- [90 Days Deep Learning (Bangla)](https://www.youtube.com/playlist?list=PLKdU0fuY4OFdFUCFcUp-7VD4bLXr50hgb)
- [PyTorch Official Tutorials](https://pytorch.org/tutorials/)
- [fast.ai Practical Deep Learning for Coders](https://course.fast.ai/)
- [Deep Learning Specialization — Andrew Ng (Coursera)](https://www.deeplearning.ai/courses/deep-learning-specialization/)
