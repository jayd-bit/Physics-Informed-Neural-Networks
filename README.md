# Physics-Informed Neural Networks (PINNs)

This project demonstrates the implementation of **Physics-Informed Neural Networks (PINNs)** in PyTorch for solving physics-based problems, such as the motion of a particle under gravity (free fall governed by the wave/ODE equation). 

### 🚀 Features
- Combines data-driven learning with physical constraints (PDE/ODE residuals).
- Implements a simple feed-forward neural network to approximate solutions. 
- Loss function includes:
  - Data loss (fit experimental/simulated data)
  - Physics loss (ODE/PDE residuals)
  - Initial/boundary condition loss
- Example: predicting height of a free-falling object using Newton’s law of motion.

### 🛠️ Tech Stack
- Python  
- PyTorch  
- NumPy / Matplotlib  

### 📂 Project Structure
- `data_generation.py` → Synthetic dataset (free-fall motion)  
- `model.py` → PINN architecture (MLP with Tanh activation)  
- `losses.py` → Data, physics, and IC loss functions  
- `train.py` → Training loop with combined loss  
- `notebooks/` → Jupyter notebook examples  

### ▶️ Usage
```bash
git clone https://github.com/your-username/pinns-project.git
cd pinns-project
python train.py
