# Dataset Directory

This directory should contain the MonkeyPox skin lesion dataset for training and evaluation. However, the actual dataset files are not included in this repository due to their large size (several GB).

## 📊 About the Dataset

This project uses the **MonkeyPox Skin Lesion Dataset** which contains images of skin lesions categorized as:
- **Monkeypox**: Images showing monkeypox symptoms
- **Non-Monkeypox**: Images of other skin conditions or normal skin

## 📥 How to Download the Dataset

### From Kaggle (Recommended)

1. **Visit the dataset page:**
   ```
   https://www.kaggle.com/datasets/nafin59/monkeypox-skin-lesion-dataset
   ```

2. **Download the dataset:**
   - Click the "Download" button on the Kaggle page
   - You may need to create a free Kaggle account if you don't have one
   - Accept the dataset license terms

3. **Extract the files:**
   ```bash
   # Extract the downloaded zip file to this directory
   unzip monkeypox-skin-lesion-dataset.zip -d dataset/
   ```

### Alternative: Using Kaggle API

If you have the Kaggle API installed:

```bash
# Install Kaggle API
pip install kaggle

# Configure your API credentials (see Kaggle documentation)
# Download the dataset
kaggle datasets download -d nafin59/monkeypox-skin-lesion-dataset

# Extract to the dataset directory
unzip monkeypox-skin-lesion-dataset.zip -d dataset/
```

## 📁 Expected Directory Structure

After downloading and extracting, your dataset folder should look like this:

```
dataset/
├── README.md                          # This file
├── Monkeypox_Dataset_metadata.csv     # Dataset metadata (included in repo)
├── Augmented Images/                   # Data-augmented training images
│   ├── Monkeypox/
│   │   ├── M01_01_00.jpg
│   │   ├── M01_01_01.jpg
│   │   └── ...
│   └── Non Monkeypox/
│       ├── NM01_01_00.jpg
│       └── ...
├── Original Images/                    # Original dataset images
│   ├── Monkeypox/
│   └── Non Monkeypox/
├── Fold1/                             # Cross-validation fold data
│   └── Fold1/
├── train_data/                        # Will be created by preprocessing
├── validation_data/                   # Will be created by preprocessing
└── test_data/                         # Will be created by preprocessing
```

## 🔧 After Download

Once you've downloaded the dataset:

1. **Verify the structure** matches the expected layout above
2. **Run the preprocessing notebook** (`model_preprocessing.ipynb`) to:
   - Split data into train/validation/test sets
   - Set up data generators for training
3. **Start training** your models!

## 📊 Dataset Statistics

- **Total Images**: ~1,000+ images
- **Classes**: 2 (Monkeypox, Non-Monkeypox)
- **Image Format**: JPG
- **Image Size**: Variable (will be resized to 224x224 for training)
- **Data Split**: 60% train, 20% validation, 20% test (configured in preprocessing)

## ⚠️ Important Notes

### Dataset License & Usage
- Please respect the dataset license terms on Kaggle
- This dataset is for research and educational purposes
- Cite the original dataset creators in any publications

### Privacy & Ethics
- This dataset contains medical imaging data
- Use responsibly and in compliance with medical data guidelines
- Models trained on this data should not be used for actual medical diagnosis

### Data Quality
- Review the data for any quality issues
- Consider data augmentation for better model generalization
- Validate model performance on multiple test scenarios

## 🆘 Troubleshooting

### Common Issues:

1. **Large download size**: The dataset is several GB - ensure you have sufficient storage and bandwidth

2. **Kaggle account required**: You need a free Kaggle account to download the dataset

3. **Extraction problems**: Make sure you have enough disk space and proper permissions

4. **Path issues**: Ensure the extracted files match the expected directory structure

### Need Help?

- Check the main repository README for additional guidance
- Review the preprocessing notebook for data handling examples
- Open an issue on the GitHub repository if you encounter problems

## 📝 Dataset Citation

If you use this dataset in your research, please cite:

```
MonkeyPox Skin Lesion Dataset
Available at: https://www.kaggle.com/datasets/nafin59/monkeypox-skin-lesion-dataset
```

## 🔗 Useful Links

- [Kaggle Dataset Page](https://www.kaggle.com/datasets/nafin59/monkeypox-skin-lesion-dataset)
- [Kaggle API Documentation](https://github.com/Kaggle/kaggle-api)
- [Main Project Repository](https://github.com/geeky-brahma/MonkeyPoxPrediction)
