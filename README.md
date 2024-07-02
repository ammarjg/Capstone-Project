# Capstone Project: Earthquake Emergency Response Robots

## Project Purpose

Define the specific requirements (size, sensors, capacity, water resistance, etc.) for the earthquake emergency response robots. Investigate the availability and efficiency of off-the-shelf alternatives.

## Project Description

Cost and time-efficient production requirements for Earthquake Emergency Response Robots.

## Project Requirements

**Earthquake Emergency Response Robot Specifications:**
- Communication accessories such as camera, microphone, speakers.
- Heat map and sound detection gadgets inclusion.
- Air quality detection systems (Carbon monoxide, oxygen, etc. levels).
- Adaptable accessories such as hydraulic lift, stretcher, tray, solar panels, etc.
- Site/route mapping via communication between robots and AI.

## Project Standards and Constraints

There are constraints such as time, cost, technology, hardware implementation, etc. for this project.

## Responsibilities of the Lead (Computer Engineering) Department Students

- Investigate alternative and heuristic-based approaches for robust robot paths.
- Investigate alternative and heuristic-based approaches for vehicle power optimization.
- Software implementation utilizing software programs like Matlab, Python, etc.

## Responsibilities of the Industrial Engineering Department Students

- Investigate efficient robot paths using operational research and optimization techniques.
- Investigate vehicle power optimization.

## Responsibilities of the Civil Engineering Department Students

- Define the earthquake emergency response robots' requirements (size, sensors, capacity such as tonnage, power supply, etc.).
- Research currently available alternatives.
- Create a database to be shared with the other team members.

## Responsibilities of the Artificial Intelligence Department Students

Applying machine learning techniques for classification of the environmental noises.

## Contributions of Artificial Intelligence Department Students

### Introduction

Since earthquakes are so damaging and produce such dangerous situations, they present serious obstacles to search and rescue efforts. The aim of this capstone project was to create a complex machine learning model for sound classification to help Earthquake Emergency Response Robots locate and identify survivors in an earthquake situation. This section covers the research and developments of our goals, methods, findings, and implications for further work.

### Objectives

The primary objectives of this project were:

1. **Data Collection and Preprocessing**: Gather datasets of environmental sounds related to earthquakes (structural damage, human presence, emergency signal noises) and preprocess these datasets for model training and optimization.
2. **Model Selection and Development**: Choose Convolutional Neural Networks (CNNs) and Recurrent Neural Networks (RNNs) as the main algorithms for our sound classification model. Develop, train, and evaluate the model to achieve high accuracy.
3. **Integrated System Development**: Combine the CNN and RNN models to create a system capable of classifying environmental sounds in real-time.
4. **Real-World Validation**: Test the model's performance in simulated earthquake scenarios using a variety of sounds to evaluate its effectiveness and accuracy in real-world situations.

### Methodology

**Data Collection and Preprocessing**

We started by gathering existing datasets like ESC-50 and UrbanSound8K from Kaggle, which include common sounds such as screams and structural destruction noises. Due to limited data, we also created a new dataset using audio samples from internet repositories for better model training.

Data preprocessing involved:

- **Normalization**: Standardizing audio features to remove biases and ensure consistent input.
- **Resampling**: Ensuring all audio samples have a uniform rate.
- **Spectrogram Generation**: Converting audio samples into spectrogram representations for CNN input.
- **Data Augmentation**: Applying techniques like time shifting and pitch shifting to improve model robustness.

**Model Selection and Justification**

Research indicates CNNs and RNNs perform well in audio classification tasks (Piczak 2015; Hershey et al. 2017). CNNs are adept at identifying noises connected to structural damage by extracting local features from spectrograms. RNNs excel at recognizing human vocalizations and other dynamic noises by modeling temporal dependencies.

**Model Development**

We built separate CNN and RNN models for classifying structural and human sounds. The CNN model consists of multiple convolutional layers followed by fully connected layers, while the RNN model uses a Long Short-Term Memory (LSTM) architecture. The models were trained using cross-entropy loss and Adam optimization.

**Integrated System Development**

The integrated CNN-RNN system operates as follows:

1. **Audio Input**: Environmental sounds are captured by the robot's microphone.
2. **Preprocessing**: The audio undergoes normalization and resampling.
3. **Feature Extraction**: The CNN model extracts relevant features from the spectrogram.
4. **Temporal Analysis**: The RNN model analyzes temporal patterns to identify sound categories.
5. **Classification**: The model classifies the sound category (e.g., "human voice," "collapsing structure," "emergency signal").

### Real-World Validation

The model was tested in simulated earthquake environments with various noise sources, including structural damage, human activity, and emergency signals. Rigorous testing validated the model's accuracy and adaptability, confirming its suitability for deployment in Earthquake Emergency Response Robots.

### Results

Our integrated CNN-RNN sound classification system achieved high accuracy in identifying and classifying relevant sounds in simulated earthquake scenarios. Key results include:

- **Locating Survivors**: Accurately detected human voices and calls for help in noisy environments.
- **Assessing Structural Damage**: Effectively classified sounds associated with collapsing structures and debris.

### Conclusion

The development of our sound classification model represents a significant advancement in disaster response technology. By combining CNNs and RNNs, we've created a robust model capable of real-time sound classification. Integrated into Earthquake Emergency Response Robots, this model enhances situational awareness and aids rescue efforts by accurately identifying and locating survivors, as well as assessing structural damage.

## References

Please refer to our final project report for detailed methodologies, experimental results, and comprehensive analysis.
