# VQE-based Integer Factorization

This project implements a hybrid quantum-classical algorithm using the Variational Quantum Eigensolver (VQE) to factorize composite numbers, specifically **N = 35**, using **Qiskit**. The notebook guides users through constructing a variational ansatz, defining a cost function, evaluating quantum measurements, and applying classical optimizers.

---

## Table of Contents

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

## Introduction

This notebook applies the **Variational Quantum Eigensolver (VQE)** to factor the number 35 by minimizing a cost function derived from the expression \((x \times y - N)^2\), where \(x\) and \(y\) are encoded in qubits. The algorithm uses quantum circuits to evaluate expectations and classical optimizers to update parameters.

---

## Features

- Implements VQE for integer factorization
- Custom cost function based on binary multiplication
- Supports multiple classical optimizers from `qiskit_algorithms`
- Compatible with Qiskit Aer simulators
- Visual output and convergence plots

---

## Installation

### Step-by-Step Setup

```bash
# Clone the repository
git clone https://github.com/xiaowei9836/VQE-based-Integer-Factorization.git
cd VQE-based-Integer-Factorization

# Create and activate a virtual environment
python -m venv vqe-env
source vqe-env/bin/activate  # On Windows: vqe-env\Scripts\activate

# Install dependencies
pip install qiskit qiskit-aer qiskit-algorithms numpy matplotlib
```

---

## Usage

### Open and run the notebook:
```bash
jupyter notebook vqe_factorization_n35_modified_2.ipynb
```

1.	Step through the cells to initialize the ansatz
2.	Define the cost function and optimization objective
3.	Execute the classical optimization loop
4.	Analyze the output bitstrings to recover factors of 35

---

## Configuration

- Adjust the number of qubits for larger factorizations.
- Choose different optimizers like COBYLA, SPSA, or L_BFGS_B via Qiskit’s optimizer API.
- Configure parameters and iterations at the optimizer level.

---

## Dependencies

- python ≥ 3.8
- qiskit ≥ 0.44
- qiskit Aer
- qiskit-algorithms
- numPy
- matplotlib
  Optional:
  ```bash
  pip install jupyter
  ```

---

## Examples

After running optimization, the notebook prints measurement results and displays convergence plots. For N = 35, you should observe that the optimized bitstrings decode to the factors 5 and 7.

---

## Troubleshooting

- **Import Errors**: Ensure all Qiskit components and optimizers are installed correctly.
- **Slow Convergence**: Try switching optimizers or increasing iterations.
- **Simulator Errors**: Verify Qiskit Aer is installed and your Python environment is compatible.

---

## Contributors

- xiaowei9836 – Initial work, algorithm design, and implementation

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.
