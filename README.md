# Video Classification Project: Shoplifting Detection Using AI

## Overview

This project implements an AI system to detect potential shoplifting in real-time using video classification. The system is built using the `VideoMAE` model to analyze video footage and classify it into one of two categories: **Shoplifting** or **Non-shoplifting**.

### Key Features:
- **Preprocessing**: Video data is preprocessed through frame extraction and normalization.
- **Model**: Uses the `VideoMAE` architecture to learn spatio-temporal features.
- **Binary Classification**: Converts model logits into a binary classification (Shoplifting or Not Shoplifting).
- **Evaluation Metrics**: Training is evaluated using F1 scores, accuracy, and validation loss.
- **Edge Deployment**: The model can be optimized with TensorFlow Lite for real-time use on devices like Raspberry Pi.


## Project Structure

```bash
.
├── data/
│   ├── Shop Lifters/         # Training dataset
│   └── Non shopLifters/      # Validation dataset
├── models/
│   ├── pre_trained_video_classify.py   # VideoMAE model implementation
│   └──shoplifters_classifier.py  # Video classification model using a model from scratch
├── classify_1/
│   ├── __pycache__/    
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── __init__.py
├── videoApi/
│   ├── __pycache__/    
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── __init__.py
├── Templates/
│   ├── upload.html
│   └── result.html
```

### Preprocessing:
DataSet Preprocess: modify the data set to be loaded in a list then splitted into three sections Train,Validation and Test
Frame extraction: Extracts individual frames from videos.
Normalization & Resizing: Normalizes pixel values and resizes frames to the input dimensions for the VideoMAE model.

### Evaluation:
The model is evaluated after every epoch, showing:
F1 Score
Accuracy
Validation Loss
this information was used to monitor training progress and avoid overfitting.

### Future Improvements
Real-Time Deployment: Convert the model into TensorFlow Lite for deployment on edge devices like Raspberry Pi.
Complex Behavior Detection: Extend the model to detect other behaviors in retail settings.
### Conclusion
This project serves as a foundation for developing an AI-based video classification system that can be used to detect shoplifting in real-time. It leverages advanced deep learning models and preprocessing techniques to ensure high accuracy and efficiency.

