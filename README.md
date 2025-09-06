# Physics-Informed Neural Networks (PINN):

This repository demonstrates a simple implementation of **Physics-Informed Neural Networks (PINNs)** using PyTorch. The goal is to solve the motion of a falling object under gravity, combining noisy data with physical laws (ODE constraints).

Motivation

Ideal for learners exploring model-based scientific machine learning and neural differential equation methods.
---

## 🔹 Problem Setup

We model the height of an object under gravity:

\[
h(t) = h_0 + v_0 t - \frac{1}{2} g t^2
\]

- **h0**: Initial height  
- **v0**: Initial velocity  
- **g**: Acceleration due to gravity  

The PINN learns to approximate \(h(t)\) by minimizing:  
- **Data loss** → Fit noisy measurements  
- **Physics loss** → Enforce ODE constraint (dh/dt = v0 - g t)  
- **Initial condition loss** → Enforce h(0) = h0  

---

## 🔹 Features

- Generates synthetic noisy data  
- Defines a simple feed-forward neural network (MLP) for \(h(t)\)  
- Uses **automatic differentiation** to compute derivatives  
- Implements a **combined loss** with physics, data, and initial condition terms  
- Trains the network to approximate the free-fall trajectory  
- Plots:
  - Exact analytical solution  
  - Noisy synthetic data  
  - PINN prediction  

---

## 🔹 Requirements

- Python 3.8+  
- PyTorch  
- NumPy  
- Matplotlib  

Install dependencies:  

```bash
pip install torch numpy matplotlib

🔹 Usage:

Clone and run:

git clone https://github.com/your-username/pinns-freefall.git
cd pinns-freefall
python pinn_freefall.py


You’ll see training progress and a plot comparing PINN predictions vs true solution vs noisy data.

🔹 Results:

PINN learns to fit noisy data while respecting physical laws.

Even with small data, the model generalizes well because of the physics constraints.

<p align="center"> <img src="docs/pinn_plot.png" width="500"> </p>

🔹 Future Work:

Extend to PDEs (e.g., wave equation, heat equation).

Apply to real-world physics problems (acoustics, fluid dynamics).

Experiment with deeper networks and advanced optimizers.

🔹 References:

Raissi, M., Perdikaris, P., & Karniadakis, G. E. (2019). Physics-informed neural networks: A deep learning framework for solving forward and inverse problems involving nonlinear partial differential equations.

Add a Friendly Disclaimer About Handwritten Notes:

If you plan to show handwritten notes in your repo, you can add a subtle disclaimer like:

Note: My handwriting may not be perfect, but the notes are thoughtfully arranged and insightful—hope you find them helpful

![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/github/license/jayd-bit/Physics-Informed-Neural-Networks)
