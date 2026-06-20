# Speech Emotion Detection

## About the Project

This project explores how machine learning can be used to identify emotions from human speech. While people can usually tell whether someone sounds happy, sad, angry, or calm just by listening, teaching a computer to do the same is a much more challenging task.

The goal of this project was to build a model that can classify emotions from speech recordings by extracting meaningful audio features and training a machine learning classifier on those features.

This project was developed as part of my learning journey in machine learning, audio processing, and model evaluation.

---

## Dataset

The model was trained using the RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song) dataset.

The dataset contains speech recordings performed by professional actors expressing different emotions. Each audio sample is labeled with its corresponding emotion, making it suitable for supervised machine learning tasks.

The emotions included in the dataset are:

* Neutral
* Calm
* Happy
* Sad
* Angry
* Fearful
* Disgust
* Surprised

---

Emotions used in code 

"emotion_dict = {
    '01': 'neutral',
    '03': 'happy',
    '04': 'sad',
    '05': 'angry'
}"

---

## Approach

The project follows a typical machine learning workflow for audio classification.

1. Audio files are loaded using Librosa.
2. Relevant speech features are extracted from each recording.
3. The extracted features are cleaned and prepared for training.
4. Important features are selected to reduce noise and improve performance.
5. Features are scaled before model training.
6. A Support Vector Machine (SVM) classifier is trained on the processed data.
7. The model is evaluated using standard classification metrics.

---

## Features Used

Rather than feeding raw audio directly into the model, several audio features are extracted to represent the speech signal in a more meaningful way.

### MFCCs

Mel-Frequency Cepstral Coefficients (MFCCs) are commonly used in speech recognition and audio analysis. They capture important characteristics of human speech and form the core feature set of this project.

### Delta MFCCs

These features represent the rate of change of MFCC values over time and help capture speech dynamics.

### Delta-Delta MFCCs

These capture the acceleration of feature changes and provide additional temporal information.

### Statistical Features

Summary statistics such as mean and standard deviation are used to create a compact representation of the extracted audio features.

---

## Model

A Support Vector Machine (SVM) classifier was used for emotion classification.

SVM was chosen because it performs well on high-dimensional datasets and often provides strong results for classification problems where the number of features is relatively large.

---

## Workflow

RAVDESS Audio Dataset

↓

Audio Loading (Librosa)

↓

Feature Extraction

(MFCC, Delta MFCC, Delta-Delta MFCC)

↓

Feature Selection

↓

Feature Scaling

↓

Train-Test Split

↓

SVM Training

↓

Model Evaluation

↓

Emotion Prediction

---

## Results

The model was evaluated on a separate test dataset after feature extraction, preprocessing, and training.

### Model Performance

- Model: Support Vector Machine (SVM)
- Features Used:
  - MFCC
  - Delta MFCC
  - Delta-Delta MFCC
- Test Accuracy: 72%

The results demonstrate that meaningful emotional patterns can be extracted from speech recordings using traditional machine learning techniques. While there is room for improvement, the model was able to classify emotions with reasonable accuracy and provided valuable insights into speech-based emotion recognition.

## What I Learned

Working on this project helped me gain practical experience in:

* Audio signal processing
* Feature engineering
* Machine learning pipelines
* Model evaluation
* Speech emotion recognition
* Using Librosa for audio analysis
* Organizing machine learning projects with Git and GitHub

It was also my first deeper exposure to working with audio data instead of traditional tabular datasets.

---

## Future Improvements

Some improvements I would like to explore in future versions include:

* Real-time emotion detection using microphone input
* Deep learning models such as CNNs and LSTMs
* A web interface for easier interaction
* Better handling of noisy audio samples
* Support for additional speech datasets

---

## Technologies Used

* Python
* NumPy
* Pandas
* Librosa
* Scikit-Learn
* Matplotlib
* Seaborn
* Jupyter Notebook
* Git
* GitHub

---
