# VQE-based Integer Factorization

This project implements a hybrid quantum-classical algorithm using the Variational Quantum Eigensolver (VQE) to factorize composite numbers, specifically **N = 35**, using **Qiskit**. The notebook guides users through constructing a variational ansatz, defining a cost function, evaluating quantum measurements, and applying classical optimizers.

---

## 📚 Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Dependencies](#dependencies)
- [Examples](#examples)
- [Troubleshooting](#troubleshooting)
- [Contributors](#contributors)
- [License](#license)

---

## 🧠 Introduction

This notebook applies the **Variational Quantum Eigensolver (VQE)** to factor the number 35 by minimizing a cost function derived from the expression \((x \times y - N)^2\), where \(x\) and \(y\) are encoded in qubits. The algorithm uses quantum circuits to evaluate expectations and classical optimizers to update parameters.

---

## ✨ Features

- Implements VQE for integer factorization
- Custom cost function based on binary multiplication
- Supports multiple classical optimizers from `qiskit_algorithms`
- Compatible with Qiskit Aer simulators
- Visual output and convergence plots

---

## 💻 Installation

### Step-by-Step Setup

```bash
# Clone the repository or download the notebook
git clone https://github.com/xiaowei9836/VQE-based-Integer-Factorization.git
cd vqe-factorization

# Create and activate a virtual environment
python -m venv vqe-env
source vqe-env/bin/activate  # On Windows: vqe-env\Scripts\activate

# Install dependencies
pip install qiskit qiskit-aer qiskit-algorithms numpy matplotlib
