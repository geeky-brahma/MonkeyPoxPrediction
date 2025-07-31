# Models Directory

This directory contains the trained deep learning models for MonkeyPox image classification. However, the actual model files are not included in this repository due to GitHub's file size constraints.

## 📁 Expected Model Files

The following model files should be present in this directory after training:

- `resnet50_monkeypox_model.h5` (~98 MB)
- `vgg16_monkeypox_model.h5` (~528 MB) 
- `mobilenetv2_monkeypox_model.h5` (~14 MB)

## 🚀 How to Generate the Models

To create these model files, follow these steps:

### Prerequisites
1. Ensure you have the required dependencies installed:
   ```bash
   pip install -r requirements.txt
   ```

2. Prepare your dataset in the correct structure (see main README.md for details)

### Training Process
1. **Open the training notebook:**
   ```bash
   jupyter notebook model_preprocessing.ipynb
   ```

2. **Run all cells in sequence** to:
   - Split the dataset into train/validation/test sets
   - Create the three model architectures (ResNet50, VGG16, MobileNetV2)
   - Train each model for 10 epochs
   - Save the trained models to this directory

3. **Training time estimates:**
   - **CPU only**: 2-4 hours per model
   - **GPU accelerated**: 20-40 minutes per model

### Alternative: Download Pre-trained Models

If you don't want to train from scratch, you can:

1. **Download from our releases** (if available):
   - Check the [Releases page](https://github.com/geeky-brahma/MonkeyPoxPrediction/releases) for pre-trained models

2. **Use transfer learning approach:**
   - The models use pre-trained ImageNet weights
   - Only the final classification layer needs training
   - This significantly reduces training time

## 🔧 Using the Models

Once you have the model files, you can use them for inference:

```python
import tensorflow as tf

# Load a specific model
model = tf.keras.models.load_model('models/mobilenetv2_monkeypox_model.h5')

# Make predictions (see model_run.ipynb for complete example)
prediction = model.predict(preprocessed_image)
```

## 📊 Model Performance

After training, update this section with your results:

| Model | Accuracy | File Size | Training Time |
|-------|----------|-----------|---------------|
| ResNet50 | TBD | ~98MB | TBD |
| VGG16 | TBD | ~528MB | TBD |
| MobileNetV2 | TBD | ~14MB | TBD |

## 💡 Tips

- **MobileNetV2** is recommended for deployment due to its smaller size and faster inference
- **ResNet50** typically provides the best accuracy for medical imaging tasks
- **VGG16** is the largest model but may provide good results for complex cases

## ⚠️ Important Notes

- Models are trained on medical imaging data - use responsibly
- Always validate model performance on your specific dataset
- Consider fine-tuning for better performance on your use case
- These models are for research/educational purposes only

## 🆘 Need Help?

If you encounter issues during training:
1. Check the main repository issues page
2. Ensure your dataset is properly formatted
3. Verify you have sufficient computational resources
4. Consider reducing batch size if you encounter memory errors
