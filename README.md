🔐 CAPTCHA Breaker — CST463 Project Proposal
👥 Team Members

Carlos Guizar

Daniel Solano

Mariana Duran

💡 Project Idea

Our project focuses on building a model capable of solving CAPTCHA images. These distorted text images are designed to distinguish humans from bots — naturally, we took that as a challenge.

The goal:
Build a deep learning pipeline that can recognize alphanumeric CAPTCHA text using modern computer vision and sequence-modeling techniques.

📚 Dataset

We plan to use the CAPTCHA Version 2 dataset from Kaggle:

🔗 https://www.kaggle.com/datasets/fournierp/captcha-version-2-images/data

This dataset contains numerous labeled CAPTCHA images featuring randomized:

  - Fonts
  
  - Character spacing
  
  - Distortions
  
  - Background noise

Perfect for training models to survive visual chaos.

🧠 Model Architecture

We will combine:

1️⃣ Convolutional Neural Networks (CNNs)

Used for feature extraction. CNNs help the model learn:

  - Character edges
  
  - Shapes
  
  - Noise patterns
  
  - Distortion adjustments

2️⃣ Recurrent Neural Networks (RNNs)

Specifically something like LSTM or GRU to decode the sequence of characters after the CNN extracts spatial features.

Together, the system works like:

CNN → Feature Map → RNN → Character Sequence Output
Basically: “Find letters, then read them in order.”

🎨 Data Augmentation Techniques

  - To improve robustness and prevent overfitting, we’ll apply:

  - Small translations (random shift in x/y by a few pixels)

  - Small rotations (±10° so things don’t spin into orbit)

  - Slight scaling and shearing

0 Random lines/points to simulate CAPTCHA clutter

This helps the model handle the wild variations found in real CAPTCHA systems.

🖥️ Computational Requirements

Training will be performed using Google Colab, taking advantage of:

  - Free GPU resources

  - Easy notebook collaboration

  - Direct Kaggle API integration for dataset access

  - For more intensive experiments (if needed), we may explore:

  - TPU runtimes

Colab Pro

Local GPU training setups

🚀 Planned Outcomes

By the end of the project, we expect to have:

A trained model capable of predicting CAPTCHA text

Evaluation metrics (accuracy, character error rate, etc.)

A demo notebook showing end-to-end CAPTCHA decoding

A polished final report and presentation
