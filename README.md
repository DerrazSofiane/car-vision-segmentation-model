# Car Vision Segmentation Model 🚗

## OpenClassrooms Project 8: Computer Vision for Autonomous Vehicles

### 📋 Project Overview
Development of a semantic segmentation model for Future Vision Transport's autonomous vehicle system. This project implements state-of-the-art computer vision techniques to identify and segment various objects in urban driving scenarios.

### 🎯 Objectives
- Build semantic segmentation models for autonomous driving
- Compare different architectures (FCN, U-Net, DeepLab, etc.)
- Deploy model via Flask API
- Create web interface for demonstration

### 📊 Dataset
- **Source**: Cityscapes Dataset
- **Training Images**: 2,975
- **Validation Images**: 500
- **Test Images**: 1,525
- **Classes**: 30+ urban scene categories (vehicles, pedestrians, road, etc.)
- **Resolution**: High-resolution urban street scenes

### 🛠️ Technical Stack
- **Python 3.x**
- **Deep Learning Framework**: TensorFlow/Keras or PyTorch
- **Computer Vision**: OpenCV
- **Deployment**: Flask API
- **Web App**: Separate repository
- **Containerization**: Docker

### 📁 Repository Structure
```
car-vision-segmentation-model/
├── Derraz_Sofiane_1_052022.ipynb              # Main segmentation notebook
├── Derraz_Sofiane_2_API_052022.py             # Flask API implementation
├── Derraz_Sofiane_4_note_technique_052022.pdf # Technical documentation
├── Derraz_Sofiane_5_presentation_052022.pptx  # Project presentation
├── requirements.txt                            # Python dependencies
└── README.md                                   # This file
```

### 🏗️ Architecture Exploration
The project explores multiple segmentation architectures:
- **FCN** (Fully Convolutional Network) - Baseline
- **U-Net** - Encoder-decoder with skip connections
- **DeepLab** - Atrous convolutions for multi-scale features
- **PSPNet** - Pyramid pooling for global context

### 🔧 Key Features

#### Data Augmentation
- Horizontal flipping
- Brightness/contrast adjustments
- Weather simulation (fog, rain)
- Rotation and scaling

#### Model Training
- Multi-architecture comparison
- Cross-entropy + Dice loss combination
- Learning rate scheduling
- Early stopping

#### API Endpoints
```python
POST /predict
- Input: Image file
- Output: Segmentation mask + detected classes
```

### 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/DerrazSofiane/car-vision-segmentation-model.git
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook for model training:
   ```bash
   jupyter notebook Derraz_Sofiane_1_052022.ipynb
   ```

4. Launch the API:
   ```bash
   python Derraz_Sofiane_2_API_052022.py
   ```

### 🔗 Related Repositories
- **API Implementation**: [segmentation-API](https://github.com/DerrazSofiane/segmentation-API)
- **Web Application**: [segmentattion-webapp](https://github.com/DerrazSofiane/segmentattion-webapp)

### 📊 Performance Metrics
- **Mean IoU**: Target 0.75+ across all classes
- **Inference Time**: <100ms per image
- **API Response**: <200ms including preprocessing

### 🎯 Safety-Critical Focus
Special attention to:
- High recall for pedestrian detection
- Robust performance in various weather conditions
- Confidence estimation for uncertain predictions

### 📈 Model Optimization
- Quantization for size reduction
- Inference optimization for real-time performance
- Edge deployment considerations

### 📝 Skills Demonstrated
- Deep Learning for Computer Vision
- Semantic Segmentation
- Model Comparison and Selection
- API Development
- Production Deployment
- Technical Documentation

### 🚀 Future Enhancements
- Real-time video segmentation
- Multi-task learning (detection + segmentation)
- Sensor fusion with LiDAR
- TensorRT optimization
- Edge device deployment

### 📚 Documentation
- Technical note (PDF) included for detailed methodology
- PowerPoint presentation for stakeholders
- API documentation in code

### ⚠️ Important Notes
- Models require GPU for optimal performance
- Large model files not included in repo (use Git LFS or download separately)
- See requirements.txt for exact dependency versions

### 🤝 Contact
Created by Sofiane Derraz as part of the OpenClassrooms AI Engineer certification program.

---
*Note: This educational project demonstrates computer vision techniques essential for autonomous vehicle development. The methodologies can be applied to real-world self-driving car systems.*
