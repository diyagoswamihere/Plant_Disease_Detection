# Plant_Disease_Detection


🌿 Plant Disease Detection using Transfer Learning
This project uses MobileNetV2 with transfer learning to classify plant diseases from leaf images. It leverages the New Plant Diseases Dataset (Augmented) from Kaggle and applies real-time image preprocessing and model evaluation techniques. The project is built using TensorFlow and Keras.

📁 Dataset
Source: Kaggle - New Plant Diseases Dataset (Augmented)
Structure:
        -train/: Training images organized in class-wise folders.
        -valid/: Validation set with similar folder structure.
        -test/: Unlabeled test images used for final predictions.
The dataset contains thousands of labeled and augmented images across multiple plant disease categories.

🧠 Model Architecture
Base Model: MobileNetV2 pre-trained on ImageNet, with the top layer removed.
Added Layers:
-GlobalAveragePooling2D
-Dropout (0.3)
-Dense output layer with softmax activation
The base model is frozen during training to retain the learned features.

🏋️‍♂️ Training
Input Shape: 224 x 224 x 3
Batch Size: 32
Loss Function: Categorical Crossentropy
Optimizer: Adam (lr = 0.0001)
Augmentation: Rotation, shifting, shearing, zooming, and flipping
Generators: Used for both training and validation sets

🧪 Evaluation
Accuracy and loss are plotted for both training and validation phases.
Confusion matrix and classification report (Precision, Recall, F1-score) are generated for test data.
Real test images are loaded, resized, normalized, and predicted.

📊 Results
The model achieves high accuracy in identifying various plant diseases. A confusion matrix and classification report are included to visualize the performance on unseen test data.
