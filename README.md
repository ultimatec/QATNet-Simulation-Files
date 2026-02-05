Reproducibility Package (Q=5)  QATNet (OD-IDS2022 & CIC-IDS2018)

This package provides the implementation and datasets required to reproduce the Q=5 (32-dim) experiments reported in our manuscript

QATNet: A Lightweight Quantum–Classical Tabular Network for Low-Latency Intrusion Detection

We include:
Two datasets (CSV) used for the reported experiments.
Two Jupyter notebooks(one per dataset) implementing the full QATNet pipeline at Q=5.

Note on reproducibility: In the paper, metrics are reported as averages over 3 random seeds.  
Running a single seed may produce slightly different numbers (typically within a small margin), depending on random initialization, splits, and hardware.

1) Contents

OD-IDS2022 (Q=5)
OD10cleaned_intrusion_dataset.csv
Q5SIMULATIONNIDS_2022_200_.ipynb  

CIC-IDS2018 (Q=5)
cleaned_data_sampled_2018.csv
QuantunCICISD200Kds2018.ipynb

2) Environment / Requirements

The experiments were originally conducted on a single GPU-enabled workstation equipped with an NVIDIA RTX A4500 GPU (Driver 550.90.07, CUDA 12.4), as described in the manuscript. Only one GPU was used to reflect realistic deployment constraints.

The provided notebooks can also be executed on other systems (Windows or Linux) with a NVIDIA GPU, or on CPU-only hardware; however, CPU execution may be significantly slower, particularly for quantum feature encoding and TabNet training.

Recommended Python
Python 3.9+ (Python 3.10 also works)

Core Libraries
The notebooks use:
numpy, pandas, scikit-learn
torch,pytorch-tabnet
pennylane(with GPU acceleration via the lightning.gpu backend when available)
matplotlib

3) Installation

Create and activate a virtual environment, then install the dependencies:
bash
pip install numpy pandas scikit-learn matplotlib
pip install torch 
pip install pytorch
pip install pennylane
