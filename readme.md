# Notebook Structure

This repository contains notebooks for two deep learning challenges:

## Timeseries Classification Challenge
**Original notebook:** `timeseries_classification.ipynb` (preserved for reference)

**Refactored notebooks:**
- `timeseries_data_visualization.ipynb` - Data loading, exploration and visualization
- `timeseries_rnn_birnn.ipynb` - Training with RNN and Bidirectional RNN models
- `timeseries_lstm_bilstm.ipynb` - Training with LSTM and Bidirectional LSTM models
- `timeseries_gru_bigru.ipynb` - Training with GRU and Bidirectional GRU models

## Pirate Pain Challenge
**Original notebook:** `pirate_pain_challenge.ipynb` (preserved for reference)

**Refactored notebooks:**
- `pirate_pain_data_visualization.ipynb` - Data loading, exploration and visualization
- `pirate_pain_training.ipynb` - Data preprocessing, model building and training

---

# How to start
### If you are in a local environment
If you want to use the GPU (NVIDIA only):
1. Make sure you have installed the NVIDIA drivers for your GPU
2. Go to pytorch website and follow the instructions to install the right version of pytorch with CUDA support: https://pytorch.org/get-started/locally/
3. delete from requirements.txt the line that says `torch` and `torchvision`

Then, follow these steps:
1. `pip install -r ./requirements.txt`
2. Go to kaggle website, click on profile settings and create an API token. This will download a `kaggle.json` file.
3. Place the `kaggle.json` file in the user home directory under the folder `.kaggle/`. For example, on Linux it would be `/home/username/.kaggle/kaggle.json`.
4. Go in the first cell of the notebook and edit the `current_dir` variable to point to the directory where you want to download the data and work on.
   - If you have Google Drive installed and mounted, you can set it to a folder in your Google Drive.
5. Run the notebook of your choice based on the task you want to work on

---
# Relevant Notes

- After importing the data, all data gets converted to a less memory intensive data type where possible.
For example, integers that fit into int8 will be converted to that type.
- there are no missing values
- some features may be useless:
  - joint_13 to joint_25 are all pretty much all zeros
  - joint_30 is constant to 0.5