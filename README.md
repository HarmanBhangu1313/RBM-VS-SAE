# RBM vs Autoencoder 

This project explores and compares Restricted Boltzmann Machines (RBM) and Autoencoders in terms of structure, working mechanism, and typical use cases in machine learning.

---

##  Project Overview  
Both RBMs and Autoencoders are popular unsupervised learning models used for feature extraction, dimensionality reduction, and data representation learning.  
This project explains their differences with intuitive explanations, visual diagrams, and example code implementations.

---

## Key Differences  

| Feature                | RBM (Restricted Boltzmann Machine) | Autoencoder |
|------------------------|--------------------------------------|------------|
| Type                   | Probabilistic graphical model       | Neural network model |
| Structure              | Visible layer ↔ Hidden layer (with undirected connections) | Encoder → Bottleneck → Decoder (fully connected layers) |
| Learning Method        | Contrastive Divergence (unsupervised) | Backpropagation (unsupervised) |
| Output Reconstruction  | Stochastic sampling-based           | Deterministic (reconstructed input) |
| Typical Use Case       | Collaborative filtering, generative modeling | Dimensionality reduction, anomaly detection |

---
##  Mathematical Intuition (RBM vs Autoencoder)

This project compares **Restricted Boltzmann Machines (RBM)** and **Autoencoders (AE)** for learning latent representations from data, commonly used in recommendation systems and dimensionality reduction.

---

### Restricted Boltzmann Machine (RBM)

An RBM is a **probabilistic generative model** with two layers:
- A visible layer (observed data)
- A hidden layer (latent features)

There are **no connections within a layer**, only between visible and hidden units.

The model learns by assigning **higher probability to observed data configurations** and lower probability to unlikely ones.

In simple terms:
- RBM learns *which hidden features explain the visible data*
- Similar inputs activate similar hidden units

Training is done using **Contrastive Divergence**, which:
- Tries to reconstruct the input
- Adjusts weights to reduce the difference between original and reconstructed data

RBMs are good at capturing **co-occurrence patterns**, which is why they work well in collaborative filtering problems.

---

### Autoencoder (AE)

An Autoencoder is a **deterministic neural network** trained to reconstruct its input.

It consists of:
- An encoder that compresses the input into a latent representation
- A decoder that reconstructs the original input from this representation

The network is trained by minimizing **reconstruction error**, meaning:
- The output should be as close as possible to the input

In simple terms:
- The autoencoder learns *what information is essential*
- Redundant or noisy details are ignored during compression

Autoencoders learn smooth, continuous representations and are easier to train than RBMs.

---

###  Key Difference in Learning Philosophy

- **RBM** learns a *probability distribution* over the data  
- **Autoencoder** learns a *deterministic mapping* for reconstruction  

RBMs model uncertainty and randomness explicitly, while autoencoders focus on minimizing reconstruction error.

---

### Why Compare RBM and Autoencoder

Both models:
- Learn latent representations
- Reduce dimensionality
- Can be used for recommendation systems

But they differ in:
- Training complexity
- Interpretability
- Stability and convergence

Comparing them highlights the trade-off between **probabilistic modeling** and **deterministic reconstruction**.

---

### Practical Insight

- RBMs can capture subtle interaction patterns but are harder to train
- Autoencoders are more stable and easier to scale
- In practice, autoencoders often replace RBMs in modern systems, but RBMs remain conceptually important

---


##  Tech Stack  
- Python 3.10  
- TensorFlow / PyTorch  
- NumPy, Pandas  
- Matplotlib, Jupyter Notebook  

---

##  Installation & Usage  

1. Clone the repo:  
   ```bash
   git clone https://github.com/harmansingh/rbm-vs-autoencoder.git


   pip install -r requirements.txt
