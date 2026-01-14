# Quantum classification of strawberry leaves
CTIC adaptation of ARQA Demo 1

## Project Structure
- dataset
  - hojas2clases: Unzip the compressed file inside here
  - HojasSimulador: Unzip the compressed file inside here
- notebooks
- src
  - nn
    - ansatz
    - encodings
    - measurements
    - models
      - hybrid
        - HQNN_Parallel.py
        - HQNN_quanv.py
      - quantum
        - QCNN.py
    - qlayers
      - quantum_linear.py
      - quanvolution.py
  - utils
    - dataset.py
    - plotting.py
    - reshape_data.py
    - run_conf.py
    - run_experiment.py
    - run_inference.py
    - training.py
  - YOLO
    - yolo_funcs.py

## Setup and Data (Releases)
The dataset and trained models are hosted in the **Releases** section of this repository. Please download the files and organize the `dataset` directory as follows:

- dataset/
  - 2hojas_HybridCNN.pth
  - 2hojas_QCNN.pth
  - best.pt
  - hojas2clases/
    - Data1/ (Unzip images here)
  - HojasSimulador/
    - Data2/ (Unzip images here)

## Usage Workflow
The correct workflow for using this project is as follows:

1. **Preprocessing:** First, create the leaf crops by running the `CropLeaves.ipynb` notebook.
2. **Model Testing:** Depending on whether you want to test the Hybrid or Quantum model, use `HQNN.ipynb` or `QCNN.ipynb` respectively.
3. **Training & Hyperparameters:** If you wish to modify the training hyperparameters for the classification models, use `TrainHQNN.ipynb` or `TrainQCNN.ipynb`.
