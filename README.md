#Personalized-Health-Care-Assistant-using-AI-ML-models

 Multimodal Mental Health Assistant

This project introduces a real-time, multimodal mental health assistant that leverages artificial intelligence to assess and support a user's emotional and psychological state using three core human interaction channels: text, voice, and facial expressions. This comprehensive approach allows the system to make accurate, context-aware assessments and respond empathetically.

 Project Overview

In an era where mental health needs real-time attention and accessibility, this assistant aims to:

Analyze user's emotional condition using multiple inputs

Recommend mental health interventions or medications

Offer a supportive chatbot response system

The assistant utilizes independent models for each modality, and integrates their outputs to offer a consolidated, personalized emotional assessment.

 Model Details and Functionalities

1. === 🔢 Text-Based Diagnosis Model

Purpose: Predict user's emotional/mental health condition from text input.

Model: Logistic Regression

Features: TF-IDF vectorized text

Classes: Depression, Anxiety, Bipolar, ADHD, Normal

Tools Used: Scikit-learn, Joblib

Outcome: Suggests relevant medications and diagnoses based on classification.

Efficiency: Very low-latency predictions suitable for real-time interaction.

Example:

Input: "I can't sleep, and my mind never stops racing."

Predicted: Anxiety → Medication Suggested: Xanax, Ativan

2. === 📸 Facial Emotion Recognition

Purpose: Recognize real-time facial expressions via webcam and detect emotion.

Model: Convolutional Neural Network (CNN)

Dataset: FER-2013 (Facial Expression Recognition)

Classes: Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral

Architecture:

Convolution + ReLU Layers

MaxPooling + Dropout Layers

Dense (Fully Connected) Layer

Input Size: 48x48 grayscale images

Efficiency: Lightweight, optimized for real-time webcam capture with Haar cascade for face detection

Example:

Input: Real-time camera detects sad expression

Output: Emotion: Sad → Chatbot responds: "I'm here for you. Want to talk about it?"

3. === 🎤 Voice Emotion Recognition

Purpose: Analyze user's vocal tone to determine emotion.

Model: Support Vector Machine (SVM)

Feature Extraction: MFCCs (Mel-Frequency Cepstral Coefficients)

Dataset: RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song)

Classes: Neutral, Calm, Happy, Sad, Angry, Fearful, Disgust, Surprised

Tools Used: Librosa, Wavio, Joblib

Efficiency: Fast audio capture (5s) with real-time prediction

Example:

Voice Input: "Just leave me alone!"

Output: Emotion: Angry → Chatbot: "Take a deep breath. Everything will be okay."

 Integration and Coherent Multimodal Workflow

While each model works independently, they are strategically integrated to offer a synchronized experience:

Text Analysis: Diagnoses mental condition and suggests medicines.

Facial Emotion Detection: Adds real-time behavioral context.

Voice Emotion Analysis: Verifies tone-based affective state.

Chatbot and Final Summary: Aggregates all data for final report and support message.

This structure ensures redundancy, consistency, and improved accuracy by cross-validating user state from multiple data sources.
