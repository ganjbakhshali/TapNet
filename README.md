# TapNet Implementation

This repository contains an initial implementation of the TapNet model as described in the paper. TapNet is a multi-task deep learning model designed to detect and classify tap events using IMU (Inertial Measurement Unit) signals from mobile devices. The model architecture is implemented based on the details provided in the paper.

## Features
- **Multi-task Model**: TapNet simultaneously performs the following tasks:
  1. Tap Event Detection (Binary Classification)
  2. Tap Direction Classification (6 Classes)
  3. Finger Part Classification (2 Classes: Fingertip or Nail)
  4. Location Classification (35 Grid Classes)
  5. Location Regression (X, Y Coordinates)
- **Architecture**: The model includes shared convolutional layers followed by fully connected layers for each task-specific branch.

## Note
This is an initial implementation, and no dataset was available to test the model's performance. The code is entirely based on the details provided in the paper. While efforts were made to ensure correctness, the lack of data for training and evaluation means the model has not been validated.

I attempted to collect sample IMU data using my own mobile device but realized that recording sufficient data for meaningful training would require more time and resources.

## Requirements
- Python 3.8+
- PyTorch 1.10+
- TorchVision
- SciPy
- torchviz (for visualizing the model)

Install dependencies using:
```bash
pip install torch torchvision scipy torchviz
```

## Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/ganjbakhshali/TapNet.git
   cd TapNet
   ```

2. Run the model:
   ```bash
   tapNet.ipynb
   ```

## File Structure
- `tapNet.ipynb`: The implementation of the TapNet model and training/testing loops.
- `README.md`: This documentation.

## Paper Reference
The implementation is based on the paper **[TapNet: The Design, Training, Implementation, and Application of Tap-Based Interaction](https://arxiv.org/abs/2102.09087)**.

## Future Work
- **Data Collection**: Record and preprocess IMU signals to test and train the model effectively.
- **Validation**: Evaluate the model's performance on a real-world dataset.
- **Optimization**: Tune the architecture and hyperparameters based on training results.



## Acknowledgments
This work is inspired by the TapNet paper and serves as a foundational implementation based on the details provided.

---
For questions or collaborations, feel free to reach out!

