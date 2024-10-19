
Video Classification Project: Shoplifting Detection Using AI
Overview
This project implements an AI system to detect potential shoplifting in real-time using video classification. The system is built using the VideoMAE model to analyze video footage and classify it into one of two categories: Shoplifting or Non-shoplifting.

Key Features:
Preprocessing: Video data is preprocessed through frame extraction and normalization.
Model: Uses the VideoMAE architecture to learn spatio-temporal features.
Binary Classification: Converts model logits into a binary classification (Shoplifting or Not Shoplifting).
Evaluation Metrics: Training is evaluated using F1 scores, accuracy, and validation loss.
Edge Deployment: The model can be optimized with TensorFlow Lite for real-time use on devices like Raspberry Pi.
Project Structure
bash
Copy code
.
├── data/
│   ├── train/         # Training dataset
│   ├── val/           # Validation dataset
│   └── test/          # Test dataset
├── models/
│   ├── video_mae.py   # VideoMAE model implementation
│   ├── preprocess.py  # Video preprocessing utilities
│   └── training_loop.py # Training and validation loops
├── notebooks/
│   └── exploration.ipynb # Exploratory Data Analysis (EDA)
├── README.md          # Project documentation
└── requirements.txt   # Python dependencies
Setup Instructions
Clone the Repository:

bash
Copy code
git clone <repository-url>
cd video-classifier
Install Dependencies: Install the necessary packages:

bash
Copy code
pip install -r requirements.txt
Prepare Dataset: Ensure your dataset is organized as follows:

bash
Copy code
data/
├── train/
│   ├── Shoplifting/
│   └── Non-shoplifting/
├── val/
│   ├── Shoplifting/
│   └── Non-shoplifting/
└── test/
    ├── Shoplifting/
    └── Non-shoplifting/
Train the Model: Train the model with the following command:

bash
Copy code
python models/training_loop.py --epochs 50 --batch_size 16 --learning_rate 0.001
Preprocessing
In the preprocess.py file:

Frame extraction: Extracts individual frames from videos.
Normalization & Resizing: Normalizes pixel values and resizes frames to the input dimensions for the VideoMAE model.
Evaluation
The model is evaluated after every epoch, showing:
F1 Score
Accuracy
Validation Loss
Use this information to monitor training progress and avoid overfitting.

How to Add New Data
Collect Videos: Label new videos as either Shoplifting or Non-shoplifting.
Organize the Dataset: Add the new videos to the corresponding subdirectories under train/, val/, or test/.
Re-train the Model:
bash
Copy code
python models/training_loop.py --epochs 50 --batch_size 16
Future Improvements
Real-Time Deployment: Convert the model into TensorFlow Lite for deployment on edge devices like Raspberry Pi.
Complex Behavior Detection: Extend the model to detect other behaviors in retail settings.
Conclusion
This project serves as a foundation for developing an AI-based video classification system that can be used to detect shoplifting in real-time. It leverages advanced deep learning models and preprocessing techniques to ensure high accuracy and efficiency.

