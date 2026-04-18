## 📂 Repository Structure

* `/implementation/` - Core FunSearch engine, Sandbox environment, and LLM API configurations.
* `/dataset/` (or `/data/`) - Standard benchmark datasets (e.g., `a280.tsp`).
* `FunSearch_TSP_main.ipynb` - The main execution notebook, containing environment setup, baseline evaluation, the FunSearch specification prompt, and post-run analysis tools.

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

## 📝 Usage Notes

* **LLM API:** Ensure your LLM API configuration inside the `config` module is properly set up with your specific provider keys.
* **Logs:** Evaluation logs and the best-generated Python scripts are automatically saved to the `funsearch_logs` directory. A helper script is included in the notebook to instantly zip and download these results.

## 🤝 Acknowledgments

This project is a group effort exploring the intersection of Large Language Models and Combinatorial Optimization, heavily inspired by DeepMind's "FunSearch" methodology.
```
