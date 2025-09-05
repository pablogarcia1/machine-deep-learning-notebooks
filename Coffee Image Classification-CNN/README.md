# Coffee Image Classification with CNN

## 📌 Project Overview
This project implements a **Convolutional Neural Network (CNN)** using TensorFlow/Keras to classify coffee-related images.  
The dataset used is self-created and very small, which means the model is heavily biased due to limited training data.  
However, with the images included in this repository, you can train, test, and validate a functional model given the available information.  


---

## 📂 Dataset
- **Training set**: 39 images  
- **Test set**: 12 images  
- Images are stored in folders (`training_set` and `test_set`) and are automatically labeled by `ImageDataGenerator`.  

Because of the dataset size, the model is not generalizable, but it still demonstrates the full workflow of:
- Data preprocessing  
- CNN training  
- Model saving/loading  
- Image prediction  

---
## Conclusion
This project demonstrates the complete workflow of training, validating, saving, and testing a CNN with TensorFlow/Keras. Even with a very small dataset, it provides a functional pipeline that can be adapted to larger and more realistic datasets.


---
## 🛠 Requirements
Make sure you have the following installed:

- Python 3.8+  
- TensorFlow / Keras  
- OpenCV  
- NumPy  
- Matplotlib  
- PIL (Pillow)  

Install dependencies with:
```bash
pip install tensorflow opencv-python numpy matplotlib pillow
