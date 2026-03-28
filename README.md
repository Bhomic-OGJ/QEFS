**QEFS: Quantum Evolutionary Feature Selector**

This repository contains the official implementation of QEFS (Quantum Evolutionary Feature Selector), a hybrid quantum–classical evolutionary algorithm for wrapper-based feature selection. The framework leverages parameterized quantum circuits to model evolutionary operators and is evaluated using both quantum simulators and real IBM quantum hardware.

**Requirements and Installation**

All required Python dependencies can be installed using:

**pip install -r requirements.txt**

The code has been tested with Python 3.8+ and Qiskit.

**Datasets**

All processed datasets used for experimental evaluation are included in this repository.

The corresponding raw datasets are publicly available from the UCI Machine Learning Repository:
https://archive.ics.uci.edu/

Dataset preprocessing follows the protocol described in the associated manuscript.

Repository Organization

The repository consists primarily of Jupyter notebooks, each implementing a specific component of the experimental study. These include:

Quantum evolutionary circuit construction

Feature encoding and measurement-based selection

Wrapper fitness evaluation using classical classifiers

Experiments on quantum simulators

Experiments on real IBM quantum hardware

Ablation and sensitivity analyses

Notebook filenames indicate the purpose of each experiment.

**IBM Quantum Execution**

If the runtime quota associated with the provided API keys is exhausted, users may generate their own API key from the IBM Quantum Platform:

https://www.ibm.com/quantum

The generated API key should be inserted into the relevant notebook cell prior to execution.

**Reproducibility and Notes**

All experiments can be reproduced using the included datasets and notebooks.

Minor variations may be observed when executing on real quantum hardware due to noise and hardware variability.

Simulator-based results are deterministic up to random seed initialization.

## Reproducibility

To ensure full reproducibility of the results reported in this work, this repository provides the complete implementation of the proposed algorithm along with all datasets used in the experiments. The codebase includes scripts for data preprocessing, model execution, evaluation, and result generation.

All experiments were conducted using a fixed set of empirically determined hyperparameters. These parameters were kept constant across all datasets to ensure fair and consistent comparison.

### Optimal Test Parameters

| Parameter | Description | Value |
|----------|------------|-------|
| **α (ALPHA)** | Error rate coefficient | 0.7 |
| **β (BETA)** | Feature count coefficient | 0.3 |
| **μ (mu)** | Mutation probability | 0.001 |
| **num_shots** | Number of quantum measurement shots | 4096 |
| **optimization_level** | Transpilation optimization level | 3 |
| **max_gen** | Maximum number of generations | 10 |
| **δ (delta)** | Population initialization angle | π / 8 |

These parameter settings were used consistently for all experiments unless stated otherwise.


Cite As:
@article{KAUSHIK2026114965,
title = {QEFS: Quantum evolutionary feature selector for a real quantum computer},
journal = {Applied Soft Computing},
volume = {194},
pages = {114965},
year = {2026},
issn = {1568-4946},
doi = {https://doi.org/10.1016/j.asoc.2026.114965},
url = {https://www.sciencedirect.com/science/article/pii/S1568494626004138},
author = {Bhomic Kaushik and Ankit Rajpal and Naveen Kumar},
keywords = {Quantum evolutionary feature selector (QEFS), Quantum gates (Hadamard Ry CNOT), IBM quantum experience, UCI machine learning repository, Quantum machine learning (QML)},
abstract = {Feature selection is a key problem in many machine learning applications. Wrapper-based feature selection algorithms help select a feature subset that optimally enhances the performance of a specific learning algorithm. However, these algorithms are highly resource-intensive, as considering all subsets of n features would require examining 2n combinations, which is a computationally infeasible task using classical computation. In contrast, quantum computing offers a more efficient representation: the entire space of feature subsets, of size |P|=2n, can be encoded using only log2⁡|P| qubits, enabling compact probabilistic representation and implicit exploration of the search space, compared to the |P| classical bits required by classical methods. Motivated by the expressive power of quantum computing, in this paper, we propose a quantum evolutionary feature selector (QEFS) and evaluate its performance on ibm_brisbane, which has been made available to the scientific community under the IBM Quantum Experience initiative. Rigorous experimentation shows that the proposed QEFS achieves accuracy comparable to that of state-of-the-art evolutionary algorithms. We demonstrate that QEFS employs a constant-depth quantum circuit, representing a significant advancement over classical feature selection approaches. Furthermore, QEFS exhibits strong robustness on real quantum hardware through effective error mitigation, achieving stable performance across multiple runs, minimal probability drift between simulator and QPU executions, and consistent behavior under varying parameter settings, as corroborated by the sensitivity analysis. The implementation of the proposed QEFS is publicly available at: https://github.com/Bhomic-OGJ/QEFS.}
}
