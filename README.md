# 🎭 Face Mask Detection System

Real-time face mask detection using Deep Learning (MobileNetV2) and OpenCV.

![Python](https://img.shields.io/badge/Python-3.12-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Accuracy](https://img.shields.io/badge/Accuracy-98%25-success)

## 🎯 Overview

Detects whether people are wearing face masks in:
- 📸 Static images
- 🎥 Real-time video (webcam)

**Accuracy: 98%** on test dataset of 767 images.

## ✨ Features

- ✅ Real-time webcam detection
- ✅ Image detection
- ✅ 98% accuracy
- ✅ Lightweight model (11MB)
- ✅ MobileNetV2 architecture

## 🚀 Installation

1. Clone repository
```bash
git clone https://github.com/SaurabhD19/facemask-detection.git
cd facemask-detection
```

2. Create virtual environment
```bash
python -m venv .venv
source .venv/bin/activate
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

4. Download face detector models
```bash
mkdir -p facedetector face_detector
curl -o facedetector/deploy.prototxt https://raw.githubusercontent.com/opencv/opencv/master/samples/dnn/face_detector/deploy.prototxt
curl -o facedetector/res10_300x300_ssd_iter_140000.caffemodel https://raw.githubusercontent.com/opencv/opencv_3rdparty/dnn_samples_face_detector_20170830/res10_300x300_ssd_iter_140000.caffemodel
ln -s facedetector face_detector
```

5. Download trained model from [Releases](https://github.com/SaurabhD19/facemask-detection/releases)

## 📖 Usage

### Detect in Image
```bash
python Detectimage.py --image path/to/image.jpg
```

### Real-time Webcam
```bash
python Detectvideo.py
```
Press `q` to quit.

### Train Model
```bash
python train_mask_detector.py -d dataset
```

## 📊 Dataset

- Total: 3,827 images
- With Mask: 1,915
- Without Mask: 1,912

## 📈 Results
```
              precision    recall  f1-score

   with_mask       0.98      0.99      0.98
without_mask       0.99      0.98      0.98

    accuracy                           0.98
```

## 🛠️ Technologies

- Python 3.12
- TensorFlow/Keras
- OpenCV
- MobileNetV2
- NumPy

## 👤 Author

**Saurabh Dubey**

- GitHub: [@SaurabhD19](https://github.com/SaurabhD19)

## 📄 License

MIT License

---

⭐ Star this repo if you found it helpful!

