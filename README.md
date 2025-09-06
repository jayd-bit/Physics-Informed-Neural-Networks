# Physics-Informed Neural Networks (PINN) – Free Fall Example

This repository demonstrates a simple implementation of **Physics-Informed Neural Networks (PINNs)** using PyTorch. The goal is to solve the motion of a falling object under gravity, combining noisy data with physical laws (ODE constraints).

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
