# MonkeyPox Image Classification

A deep learning project for classifying skin lesion images as "Monkeypox" or "Non-Monkeypox" using transfer learning with popular CNN architectures.

## 🎯 Project Overview

This project implements and compares three different pre-trained deep learning models for monkeypox detection:
- **ResNet50**
- **VGG16** 
- **MobileNetV2**

The models are trained using transfer learning techniques on a dataset of skin lesion images to classify them as either containing monkeypox symptoms or not.

## 📁 Project Structure

```
MonkeyPoxPrediction/
├── dataset/
│   ├── Augmented Images/        # Data-augmented training images
│   ├── Original Images/         # Original dataset images
│   ├── train_data/             # Training set (60%)
│   ├── validation_data/        # Validation set (20%)
│   ├── test_data/              # Test set (20%)
│   └── Monkeypox_Dataset_metadata.csv
├── models/                     # Saved trained models
│   ├── mobilenetv2_monkeypox_model.h5
│   ├── resnet50_monkeypox_model.h5
│   └── vgg16_monkeypox_model.h5
├── model_preprocessing.ipynb   # Data preparation and model training
├── model_run.ipynb            # Model inference and testing
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- TensorFlow 2.x
- Jupyter Notebook

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/MonkeyPoxPrediction.git
cd MonkeyPoxPrediction
```

2. Install the required packages:
```bash
pip install -r requirements.txt
```

3. Launch Jupyter Notebook:
```bash
jupyter notebook
```

## 📊 Dataset

The dataset contains skin lesion images categorized into two classes:
- **Monkeypox**: Images showing monkeypox symptoms
- **Non-Monkeypox**: Images of other skin conditions or normal skin

### Data Split
- **Training**: 60% of the dataset
- **Validation**: 20% of the dataset  
- **Testing**: 20% of the dataset

## 🔬 Model Architecture

### Transfer Learning Approach
All models use transfer learning with the following configuration:
- Pre-trained weights from ImageNet
- Frozen base layers (feature extraction)
- Custom classification head
- Input image size: 224×224 pixels

### Models Implemented
1. **ResNet50**: Deep residual network with skip connections
2. **VGG16**: Classic CNN with 16 layers
3. **MobileNetV2**: Lightweight model optimized for mobile devices

## 📈 Usage

### Training Models
Run the `model_preprocessing.ipynb` notebook to:
1. Prepare and split the dataset
2. Set up data augmentation
3. Train all three models
4. Save the trained models

### Making Predictions
Use the `model_run.ipynb` notebook to:
1. Load a pre-trained model
2. Preprocess input images
3. Make predictions on new images
4. Visualize results

### Example Prediction
```python
# Load model
model = tf.keras.models.load_model('models/mobilenetv2_monkeypox_model.h5')

# Predict on new image
result = predict_image('path/to/your/image.jpg')
print(f'Prediction: {result}')
```

## 🎯 Key Features

- **Multiple Model Comparison**: Compare performance across ResNet50, VGG16, and MobileNetV2
- **Data Augmentation**: Enhanced dataset with augmented images for better generalization
- **Transfer Learning**: Leverages pre-trained ImageNet weights for faster training
- **Easy Inference**: Simple interface for making predictions on new images
- **Organized Structure**: Clean separation of data, models, and code

## 📋 Model Performance

| Model | Accuracy | Size | Training Time |
|-------|----------|------|---------------|
| ResNet50 | TBD | ~98MB | TBD |
| VGG16 | TBD | ~528MB | TBD |
| MobileNetV2 | TBD | ~14MB | TBD |

*Note: Update these metrics after training completion*

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact

- **Author**: [Your Name]
- **Email**: [your.email@example.com]
- **Project Link**: [https://github.com/yourusername/MonkeyPoxPrediction](https://github.com/yourusername/MonkeyPoxPrediction)

## 🙏 Acknowledgments

- Dataset providers
- TensorFlow team for the excellent deep learning framework
- Pre-trained model authors (ResNet, VGG, MobileNet teams)

## ⚠️ Disclaimer

This project is for educational and research purposes only. It should not be used as a substitute for professional medical diagnosis. Always consult healthcare professionals for medical advice.
