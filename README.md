# Detection of Misinformation Created by Deepfake Technologies

A Digital Image Processing and Deep Learning project focused on detecting manipulated images and videos generated using modern DeepFake techniques. This project explores computer vision, image forensics, deep learning, and multimedia security to combat misinformation and protect digital authenticity. Based on research, implementation, and evaluation of both XceptionNet and MesoNet architectures. 

## Project Overview

DeepFake technology has rapidly evolved through the use of Generative Adversarial Networks (GANs) and Autoencoders, enabling the creation of highly realistic fake images and videos. These manipulated media can spread misinformation, damage reputations, influence public opinion, and undermine trust in digital content.

This project investigates multiple DeepFake detection approaches and implements deep learning based solutions capable of identifying manipulated visual content through spatial and temporal analysis. 

## Key Features

• DeepFake image detection

• DeepFake video detection

• Face extraction and preprocessing

• CNN based spatial feature extraction

• LSTM based temporal sequence analysis

• Transfer learning using XceptionNet

• Lightweight MesoNet implementation

• Frequency domain analysis using Fourier Transform

• Performance evaluation using Accuracy, Precision, Recall, F1 Score, and ROC AUC

• Deployable Python inference library

## Technologies Used

### Programming Language

* Python 3.x

### Deep Learning Frameworks

* TensorFlow
* Keras

### Computer Vision

* OpenCV

### Data Processing

* NumPy
* Matplotlib

### Development Environment

* Google Colab

### Machine Learning Models

* XceptionNet
* MesoNet
* CNN
* LSTM

## Datasets

The project utilizes industry recognized DeepFake datasets:

| Dataset         | Purpose                               |
| --------------- | ------------------------------------- |
| FaceForensics++ | Training and benchmarking             |
| DFDC            | Real world DeepFake detection         |
| Celeb DF        | Generalization testing                |
| UADFV           | MesoNet implementation and evaluation |

## Project Architecture

```text
Input Video/Image
        │
        ▼
Preprocessing
(Face Detection & Alignment)
        │
        ▼
Feature Extraction
(CNN / XceptionNet / MesoNet)
        │
        ▼
Temporal Analysis
(LSTM for Videos)
        │
        ▼
Dense Layers
        │
        ▼
Binary Classification
Real / Fake
```

## Deep Learning Models

### XceptionNet

A transfer learning based DeepFake detection model that extracts complex spatial features from facial images.

#### Advantages

* High detection accuracy
* Strong benchmark performance
* Effective feature extraction

#### Limitations

* Computationally expensive
* Dataset dependent
* Requires larger hardware resources

### MesoNet

A lightweight CNN architecture specifically designed for facial forgery detection.

#### Advantages

* Fast inference
* Resource efficient
* Suitable for deployment
* Good performance on limited hardware

#### Limitations

* Less robust on highly compressed media
* Can struggle with unseen manipulation techniques

## Methodology

### 1. Data Collection

Video datasets are collected from publicly available DeepFake benchmarks.

### 2. Frame Extraction

Videos are converted into individual image frames using OpenCV.

### 3. Face Preprocessing

* Face detection
* Face alignment
* Image resizing
* Normalization

### 4. Data Augmentation

* Rotation
* Flipping
* Scaling
* Brightness adjustments

### 5. Model Training

The extracted facial frames are used to train DeepFake detection models using Binary Cross Entropy Loss.

### 6. Evaluation

Performance is measured using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC AUC

## MesoNet Implementation

The project includes a complete implementation of the MesoNet architecture trained on the UADFV dataset. Frames were extracted from real and manipulated videos, resized to 256×256 pixels, and used for binary classification training. The trained model achieved more than 80% performance across major evaluation metrics and was exported as a reusable model. 

## Python Library Integration

The trained MesoNet model was packaged into a lightweight Python library called Hamster.

### Features

* Single function prediction
* Confidence score generation
* Easy integration into APIs
* Deployment ready architecture
* Backend friendly design

### Example

```python
from hamster import predict

result = predict("sample_image.jpg")

print(result["label"])
print(result["confidence"])
```

## Results

### XceptionNet

| Metric    | Performance |
| --------- | ----------- |
| Accuracy  | High        |
| Precision | High        |
| Recall    | High        |
| F1 Score  | High        |

### MesoNet

| Metric    | Performance |
| --------- | ----------- |
| Accuracy  | > 80%       |
| Precision | > 80%       |
| Recall    | > 80%       |
| F1 Score  | > 80%       |

The results demonstrate that both architectures are capable of detecting manipulated content effectively, with MesoNet providing an efficient alternative for low resource environments. 

## Applications

### Media Verification

Verify authenticity of digital media before publication.

### Social Media Moderation

Identify manipulated content before it spreads.

### Digital Forensics

Assist investigators in analyzing suspicious multimedia evidence.

### Journalism

Protect news organizations from misinformation campaigns.

### Cybersecurity

Detect identity fraud and synthetic media attacks.

## Future Improvements

* Transformer based architectures
* Multimodal DeepFake detection
* Audio DeepFake detection
* Real time webcam analysis
* Explainable AI visualizations
* Edge device deployment
* Mobile application integration

## Repository Structure

```text
Deepfake-Detection/
│
├── datasets/
├── preprocessing/
├── models/
│   ├── xceptionnet/
│   └── mesonet/
├── training/
├── evaluation/
├── hamster/
├── notebooks/
├── results/
├── images/
└── README.md
```

## Research Contributions

This project investigates both heavyweight and lightweight DeepFake detection architectures while addressing challenges related to model generalization, computational efficiency, and deployment readiness. It demonstrates how image processing, computer vision, and deep learning can be combined to combat misinformation in modern digital environments. 


