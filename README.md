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


Citation details will be added after publication.

Contact:
bhomic.mcs21.du@gmail.com
