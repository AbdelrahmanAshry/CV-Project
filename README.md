#PROJECT"""Video Classification - Shoplifting Detection Using AI"""
#Overview
This project aims to build an AI-powered system capable of detecting potential shoplifting events in real-time through video classification. The model is trained on videos labeled into two categories: Shoplifting and Non-shoplifting. The system leverages state-of-the-art video classification models, with VideoMAE being the model used here. The primary focus is to classify whether the behavior in the video exhibits shoplifting or normal shopping activity.

#Key Features:
Preprocessing: The video data is preprocessed using frame extraction and normalization.
Video Classification Model: Uses the VideoMAE model for encoding temporal and spatial data, which is effective for recognizing actions in video streams.
Output Transformation: The model outputs 400 logits which are transformed into a binary classification (Shoplifting or Not Shoplifting).
Evaluation Metrics: The training loop includes evaluation using F1 scores, accuracy, and validation loss to assess the model's performance during and after training.
Deployment Consideration: The model can be further optimized using TensorFlow Lite for deploying on edge devices such as Raspberry Pi for real-time video surveillance in stores.
Folder Structure:
