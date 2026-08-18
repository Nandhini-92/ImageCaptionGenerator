# ImageCaptionGenerator

An image captioning project using visual image features and an LSTM-based language model.

## Project files

- `model.ipynb` — model development and training notebook
- `model_plot.png` — model architecture visualization
- `best_model.h5` — trained Keras model
- `combined_features.pkl` — extracted feature data
- `yolov5su.pt` — YOLOv5 weights
- `.gitignore` — Git ignore configuration

## Model architecture

The model accepts a 27-token text sequence and a 6144-dimensional image feature vector. The text branch uses an Embedding layer followed by Dropout and an LSTM. The image branch uses Dropout and a Dense layer to project the 6144-dimensional image representation to 256 dimensions. The two branches are combined with an Add layer, followed by Dense layers and an 813-class output layer.

## Running

Open `model.ipynb` and update any local dataset/model paths for your environment before executing the notebook.

The dataset itself is not included in this repository.
