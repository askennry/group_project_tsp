## 📂 Repository Structure

* `/implementation/` - Core FunSearch engine, Sandbox environment, and LLM API configurations.
* `/dataset/` (or `/data/`) - Standard benchmark datasets (e.g., `a280.tsp`).
* `FunSearch_TSP_main.ipynb` - The main execution notebook, containing environment setup, baseline evaluation, the FunSearch specification prompt, and post-run analysis tools.

## 📝 Usage Notes

* **LLM API:** Ensure your LLM API configuration inside the `config` module is properly set up with your specific provider keys.
* **Logs:** Evaluation logs and the best-generated Python scripts are automatically saved to the `funsearch_logs` directory. A helper script is included in the notebook to instantly zip and download these results.
