# Brain Tumor Detection Using Deep Learning

An AI-powered medical imaging system that leverages deep learning to detect and classify brain tumors from MRI scans with high accuracy. This web-based application provides healthcare professionals and researchers with an efficient tool for preliminary tumor screening and classification.

## Overview

This system employs convolutional neural networks (CNNs) to analyze brain MRI images and identify the presence and type of tumors. The application processes medical images in real-time, delivering predictions with confidence scores to assist in diagnostic workflows.

## Features

**Automated Tumor Detection**  
Upload MRI brain scans to automatically detect the presence of tumors with advanced deep learning algorithms.

**Multi-Class Tumor Classification**  
The system classifies tumors into four distinct categories:
- **Glioma**: A type of tumor that occurs in the brain and spinal cord
- **Meningioma**: A tumor that forms on membranes covering the brain and spinal cord
- **Pituitary**: A tumor in the pituitary gland
- **No Tumor**: Healthy brain tissue with no tumor detected

**Real-Time Predictions**  
Instant analysis of uploaded MRI images with confidence scores indicating prediction reliability.

**User-Friendly Web Interface**  
Clean, responsive Bootstrap-based interface that works seamlessly across desktop and mobile devices.

**High Accuracy Model**  
Deep learning model trained on extensive MRI datasets to ensure reliable tumor detection and classification.

**Visual Feedback**  
Uploaded images are displayed alongside prediction results for easy verification and analysis.

## Technology Stack

**Backend**
- Python 3.7+
- Flask (Web Framework)
- TensorFlow/Keras (Deep Learning)
- NumPy (Numerical Computing)

**Frontend**
- HTML5
- CSS3
- Bootstrap 5.3

**Machine Learning**
- Convolutional Neural Networks (CNN)
- Image preprocessing and normalization
- Transfer learning techniques

## Installation

### Prerequisites
- Python 3.7 or higher
- pip package manager
- Virtual environment (recommended)

### Setup Instructions

1. **Clone the Repository**
```bash
git clone https://github.com/yourusername/brain-tumor-detection.git
cd brain-tumor-detection
```

2. **Create Virtual Environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install Dependencies**
```bash
pip install flask tensorflow keras numpy pillow
```

4. **Download or Train the Model**
- Place your trained model file (`model.h5`) in the `models/` directory
- Alternatively, use the provided Jupyter notebook to train your own model

5. **Create Required Directories**
```bash
mkdir uploads models
```

## Usage

### Running the Application

1. **Start the Flask Server**
```bash
python main.py
```

2. **Access the Application**
- Open your web browser
- Navigate to `http://127.0.0.1:5000/`

3. **Upload and Analyze**
- Click "Select MRI Image" to choose a brain MRI scan
- Click "Upload and Detect" to process the image
- View the prediction result with confidence score

### Training Your Own Model

Use the provided Jupyter notebook (`brain_tumour_detection_using_deep_learning.ipynb`) to:
- Load and preprocess MRI datasets
- Build and train the CNN model
- Evaluate model performance
- Save the trained model for deployment

## Project Structure

```
brain-tumor-detection/
│
├── main.py                                          # Flask application
├── brain_tumour_detection_using_deep_learning.ipynb # Model training notebook
├── templates/
│   └── index.html                                   # Web interface
├── models/
│   └── model.h5                                     # Trained model (not included)
├── uploads/                                         # Uploaded images storage
├── static/                                          # Static files (CSS, JS)
├── requirements.txt                                 # Python dependencies
└── README.md                                        # Project documentation
```

## Model Details

**Architecture**
- Convolutional Neural Networks with multiple layers
- Image input size: 128x128 pixels
- Preprocessing: Pixel normalization (0-1 range)

**Training**
- Dataset: Brain MRI images with labeled tumor types
- Training environment: Google Colab with GPU acceleration
- Image augmentation for improved generalization

**Performance**
- Multi-class classification across 4 categories
- Confidence scores provided for each prediction
- Optimized for medical imaging analysis

## How It Works

1. **Image Upload**: User uploads an MRI brain scan through the web interface
2. **Preprocessing**: Image is resized to 128x128 pixels and normalized
3. **Prediction**: The CNN model analyzes the image and generates predictions
4. **Classification**: The system identifies the tumor type or confirms no tumor
5. **Results Display**: Prediction and confidence score are shown with the uploaded image

## API Endpoints

### Main Routes

**GET /**  
Displays the main upload interface

**POST /**  
Handles image upload and returns prediction results

**GET /uploads/<filename>**  
Serves uploaded images for display

## Configuration

Edit `main.py` to customize:
- Upload folder location
- Image size for predictions
- Model path
- Class labels

## Important Notes

⚠️ **Medical Disclaimer**: This system is designed as a supportive tool for medical professionals and researchers. It should NOT be used as the sole basis for medical diagnosis or treatment decisions. Always consult qualified healthcare professionals for medical advice.

## Future Enhancements

- Integration with DICOM medical imaging standards
- Batch processing for multiple images
- Advanced visualization with tumor region highlighting
- REST API for integration with medical systems
- Model performance metrics dashboard
- Support for additional tumor types
- User authentication and case management

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Dataset providers and medical imaging communities
- TensorFlow and Keras development teams
- Flask framework contributors
- Open-source medical AI research community

## Contact

For questions, suggestions, or collaboration opportunities, please open an issue on GitHub or contact the project maintainers.

---

**Note**: This is a research and educational project. Medical imaging analysis requires professional medical expertise and should always be performed or supervised by qualified healthcare professionals.
