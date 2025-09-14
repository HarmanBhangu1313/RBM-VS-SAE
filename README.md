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
