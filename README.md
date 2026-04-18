# TSP-FunSearch: Automated Heuristic Discovery for the Traveling Salesman Problem

## 🌟 Key Features

* **Automated Code Evolution:** Utilizes an LLM to iteratively evolve a `priority` function, guiding a greedy nearest-neighbor TSP solver to escape local optima.
* **Secure Execution Sandbox:** Implements a robust `multiprocessing` sandbox with strict timeout limits (60 seconds) to safely execute and evaluate unpredictable, LLM-generated code.
* **Performance Tracking:** Automatically logs evolutionary history, tracks the convergence of the objective function (total tour distance), and extracts the best-performing heuristic.
* **Academic Ready:** Structured for reproducibility and easy integration with Google Colab, requiring zero local dependency configurations.

## 📈 Key Discoveries & Results

During our experimental runs on the `a280` TSPLIB dataset, the FunSearch pipeline successfully evolved the baseline greedy nearest-neighbor algorithm into a highly sophisticated heuristic. 

* **Baseline Distance:** ~8300
* **Evolved Distance:** **6664.0**

## 📂 Repository Structure

* `/implementation/` - Core FunSearch engine, Sandbox environment, and LLM API configurations.
* `/dataset/` (or `/data/`) - Standard benchmark datasets (e.g., `a280.tsp`).
* `FunSearch_TSP_pipeline.ipynb` - The main execution notebook, containing environment setup, baseline evaluation, the FunSearch specification prompt, and post-run analysis tools.

## 🚀 Quick Start (Google Colab)

The easiest way to run and reproduce this project is via Google Colab. The pipeline is designed to pull directly from this repository.

1. Open a new Google Colab notebook.
2. Clone this repository directly into the Colab environment:
   ```python
   import os
   import sys
   import subprocess

   REPO_URL = "[https://github.com/askennry/TSP-FunSearch.git](https://github.com/askennry/TSP-FunSearch.git)"
   WORK_DIR = "/content/TSP-FunSearch"

   subprocess.run(["git", "clone", REPO_URL, WORK_DIR])
   sys.path.append(WORK_DIR)
   ```
3. Install the required TSPLIB parser:
   ```bash
   !pip install tsplib95 -q
   ```
4. Run the pipeline defined in `FunSearch_TSP_pipeline.ipynb`.


## 🛠️ Local Setup

If you prefer to run the project locally:

1. Clone the repository:
   ```bash
   git clone [https://github.com/askennry/TSP-FunSearch.git](https://github.com/askennry/TSP-FunSearch.git)
   cd TSP-FunSearch
   ```
2. Install dependencies (ensure you have Python 3.9+):
   ```bash
   pip install numpy matplotlib tsplib95
   ```
3. Execute the pipeline script or run the Jupyter Notebook.


## 🤝 Acknowledgments

This project is a group effort exploring the intersection of Large Language Models and Combinatorial Optimization, heavily inspired by DeepMind's "FunSearch" methodology.
