# Physics-Informed Neural Networks for Scientific Problems

This repository contains my ongoing work exploring **Physics-Informed Neural Networks (PINNs)** for solving and modeling scientific and mathematical problems governed by differential equations.

The main goal of this project is to investigate how neural networks can incorporate **physical laws, mathematical models, and differential equations directly into the learning process**, providing an alternative to traditional numerical methods for scientific computing.

The repository currently contains implementations of PINNs for two problems:

* **SIRD Epidemiological Model** — application of PINNs to a compartmental epidemic model.
* **Fractional Differential Equation Model for Heartwater Disease** — application of PINNs to a fractional-order epidemiological model describing the dynamics of heartwater disease.

As the project develops, additional scientific problems and models will be added.

---

## 📌 About PINNs

Physics-Informed Neural Networks are neural networks trained not only to fit data but also to satisfy the underlying governing equations of a physical or mathematical system.

For a differential equation of the form

[
\mathcal{N}[u](x,t) = 0,
]

a PINN approximates the unknown solution using a neural network

[
u(x,t) \approx u_\theta(x,t),
]

and incorporates the differential equation into the loss function.

A typical PINN objective can be written as

[
\mathcal{L}
===========

\mathcal{L}*{\text{PDE}}
+
\mathcal{L}*{\text{IC}}
+
\mathcal{L}*{\text{BC}}
+
\mathcal{L}*{\text{data}},
]

where the different terms enforce the governing differential equation, initial conditions, boundary conditions, and available observational data.

This approach provides a framework for combining **machine learning with mathematical modeling and scientific knowledge**.

---

# 📂 Repository Structure

```text
PINNs/
│
├── SIRD/
│   ├── ...
│   └── README.md
│
├── Fractional_DE_Heartwater/
│   ├── ...
│   └── README.md
│
└── README.md
```

The repository is organized by scientific problem, with each directory containing the corresponding mathematical model, implementation, experiments, and results.

---

# 🦠 1. SIRD Model

The first project investigates the use of PINNs to solve a **SIRD epidemiological model**.

The SIRD model divides a population into four compartments:

[
S(t), \quad I(t), \quad D(t), \quad R(t),
]

representing:

* **S** — Susceptible
* **I** — Infected
* **D** — Deceased
* **R** — Recovered

The model is governed by a system of ordinary differential equations describing the evolution of these compartments over time.

The PINN is trained to approximate the solution while satisfying the governing SIRD equations and relevant initial conditions and physical constraints.

### Objectives

* Solve the SIRD system using a PINN.
* Investigate the effect of the number of collocation points on the solution.
* Enforce population conservation.
* Compare the PINN solution with conventional numerical solutions.
* Explore the suitability of PINNs for epidemiological modeling.

---

# 💧 2. Fractional Differential Equation Model — Heartwater Disease

The second project explores **fractional-order differential equations** and their application to modeling **heartwater disease**.

Fractional differential equations extend classical differential equations by allowing derivatives of non-integer order. They can provide a framework for representing systems with memory or non-local effects.

The project investigates whether PINNs can be used to approximate solutions of fractional differential equation models and how the resulting solutions compare with conventional numerical approaches.

### Objectives

* Develop a PINN framework for fractional differential equations.
* Investigate the effect of fractional derivatives on disease dynamics.
* Apply the model to heartwater disease.
* Explore numerical approximation of fractional-order systems.
* Compare PINN solutions with appropriate numerical/reference solutions.

---

# 🧠 Methodology

The general workflow used throughout the repository is:

```text
Scientific Problem
       │
       ▼
Mathematical Model
       │
       ▼
Differential Equations
       │
       ▼
PINN Formulation
       │
       ├── Initial Conditions
       ├── Boundary Conditions
       ├── Physical Constraints
       └── Observational/Data Constraints
       │
       ▼
Neural Network Training
       │
       ▼
Approximate Solution
       │
       ▼
Comparison with Numerical Methods
       │
       ▼
Analysis & Visualization
```

The neural networks are trained by minimizing a loss function constructed from the governing mathematical equations and relevant constraints.

Automatic differentiation is used to obtain the derivatives required by the differential equations.

---

# 🛠️ Technologies

The projects primarily use Python and scientific machine-learning libraries, including:

* **Python**
* **PyTorch**
* **NumPy**
* **SciPy**
* **Matplotlib**

Additional libraries may be introduced as the projects develop.

---

# 📊 Numerical Validation

An important component of these projects is comparing PINN predictions against solutions obtained using conventional numerical methods.

The comparisons focus on quantities such as:

* Solution accuracy
* Absolute and relative errors
* Training convergence
* Conservation properties
* Sensitivity to collocation points
* Effect of network architecture
* Computational cost

This allows the PINN approach to be evaluated not only as a machine-learning model but also as a **scientific computing method**.

---

# 🔬 Research Direction

This repository is part of my broader exploration of **Scientific Machine Learning (SciML)** and the intersection of:

[
\boxed{
\text{Mathematics}
+
\text{Numerical Methods}
+
\text{Machine Learning}
+
\text{Scientific Modeling}
}
]

Future work will explore the application of PINNs to additional problems involving:

* Ordinary differential equations
* Partial differential equations
* Fractional differential equations
* Epidemiological models
* Dynamical systems
* Physical and biological systems
* Inverse problems
* Parameter estimation
* Data-driven scientific modeling

---

# 🚧 Status

This repository is an **ongoing research and experimentation project**.

The implementations are continuously being improved, with emphasis on understanding the strengths, limitations, and practical challenges of PINNs for scientific problems.

---

# 📚 Motivation

Traditional numerical methods remain highly effective for solving differential equations. However, PINNs offer an interesting alternative framework in which **physical laws and mathematical constraints are embedded directly into neural-network training**.

Through these projects, I aim to better understand:

> **When, why, and how can Physics-Informed Neural Networks be useful for scientific computing?**

The repository therefore serves both as a collection of implementations and as a record of my exploration of PINNs and Scientific Machine Learning.

---

## 👤 Author

**Winner Mawuanam Komla Adufutse**

MSc Mathematical Sciences — AIMS Ghana
BSc Mathematics — Kwame Nkrumah University of Science and Technology (KNUST)

Research interests include:

* Scientific Machine Learning
* Physics-Informed Neural Networks
* Computational Mathematics
* Differential Equations
* Numerical Analysis
* Mathematical Modeling
* Machine Learning for Scientific Computing

---

## ⭐ Repository Goals

The long-term goal of this repository is to build a collection of reproducible experiments demonstrating how **PINNs can be applied to diverse scientific and mathematical problems**.

If you find the work useful or interesting, feel free to explore the individual projects and follow the development of the repository.
