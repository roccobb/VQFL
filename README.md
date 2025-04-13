# Experiments for VQFL — Quantum Week 2025 Submission

This repository contains the experiments associated with the paper submitted to the **Quantum Week 2025** conference, which is currently under review.

## Repository Structure

The repository is organized as follows:

### `exps/` — Experimental Data & Results

This folder contains **5 subfolders**, each corresponding to a different experiment described in the paper.

Each subfolder includes:

- **Data files**:
  - `data_config.json`: Specifies the parameters used to reproduce the same data configuration (e.g., test size, partition seed, permutation seed for random feature assignment to clients, etc.).
  - `data_tensors.pt`: Contains the actual data tensors used for training and testing.

- **Experiment files**:
  - 4 `.json` files with hyperparameters and the results for each experiment setup:
    - Experiments with:
      - 8 clients,
      - 1 client,
      - the same client repeated 8 times,
      - 4 clients each repeated 2 times (as described in the paper).
  - 4 `.pt` files containing the trained model weights for each experiment.

---

### `nb/` — Jupyter Notebooks

This folder contains 3 notebooks designed to generate, run, and analyze the experiments:

- `create_data_setting.ipynb`: Generates and saves various data configurations to be used in experiments.
- `run_exps.ipynb`: Handles training, testing, and saving of models for all experiments.
- `compare_exps.ipynb`: Loads experiment results and generates comparison plots.

---

## Running Experiments with Jupyter Lab

To run the experiments using **Jupyter Lab**, follow these steps:
1. **Create a virtual environment**
```bash
   python3 -m venv .venv
```
2. **Activate the virtual environment**
```bash
   source .venv/bin/activate
```
3. **Install the required dependencies**
```bash
pip install -r requirements.txt
```
4. **Install the virtual environment as a Jupyter kernel**
```bash
python -m ipykernel install --user --name=vqfl-venv
```
5. **Launch Jupyter Lab and select the vqfl-venv kernel**
```bash
jupyter lab
```
