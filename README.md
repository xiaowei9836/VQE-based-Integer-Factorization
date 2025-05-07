# VQE-based Integer Factorization

This project implements a hybrid quantum-classical algorithm using the Variational Quantum Eigensolver (VQE) to factorize composite numbers, specifically **N = 35**, using **Qiskit**. The notebook guides users through constructing a variational ansatz, defining a cost function, evaluating quantum measurements, and applying classical optimizers.

---

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Usage](#usage)
- [Configuration](#configuration)
- [Dependencies](#dependencies)
- [Contributors](#contributors)
- [License](#license)

---

## Introduction

This notebook applies the **Variational Quantum Eigensolver (VQE)** to factor the number 35 by minimizing a cost function derived from the expression \((x \times y - N)^2\), where \(x\) and \(y\) are encoded in qubits. The algorithm uses quantum circuits to evaluate expectations and classical optimizers to update parameters.

This implementation is inspired by the methodology described in **Mona Sobhani's 2024 Master Thesis** at Brandenburg University of Technology, which explores a hybrid quantum-classical approach for prime factorization using IBM's NISQ (Noisy Intermediate-Scale Quantum) devices. This work highlights how quantum circuits can be used to evaluate computationally intensive parts of the factorization problem, while classical optimizers iteratively refine solutions. This hybrid model shows promise for demonstrating early-stage quantum advantage in cryptographic applications such as RSA, and the notebook mirrors these techniques using Qiskit and Aer simulation tools.

Reference thesis: [DOI: 10.26127/BTUOpen-6814](https://opus4.kobv.de/opus4-btu/frontdoor/index/index/docId/6814)

---

## Features

- Implements VQE for integer factorization
- Custom cost function based on binary multiplication
- Supports multiple classical optimizers from `qiskit_algorithms`
- Compatible with Qiskit Aer simulators
- Visual output and convergence plots

---

## Usage

### Open and run the notebook:
  ```bash
    jupyter notebook VQE-based_Integer_Factorization.ipynb
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
- qiskit_aer
- qiskit_algorithms
- numPy
- matplotlib
- Optional:
  ```bash
    pip install jupyter
  ```

---

## Contributors

- `xiaowei9836` – Initial work, algorithm design, and implementation

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.
