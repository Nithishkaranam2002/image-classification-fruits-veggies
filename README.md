# Image Classification using Fruits and Vegetables

This project focuses on building an image classification system that accurately classifies images of fruits and vegetables using a Convolutional Neural Network (CNN) model. The model is built with Keras and TensorFlow, and the project is deployed using a simple `Flask` API for real-time inference.

---

## 🧠 Objective

To classify images into categories like apples, bananas, carrots, etc., using a CNN trained on labeled fruit and vegetable images. This project demonstrates the end-to-end ML pipeline from training to deployment.

---

## 🏗️ Architecture Overview

```
        +----------------------+
        |  User Upload Image  |
        +----------+-----------+
                   |
                   v
          +--------+--------+
          |  Flask API (app.py) |
          +--------+--------+
                   |
                   v
        +----------+-----------+
        | Load Trained CNN Model |
        +----------+-----------+
                   |
                   v
        +------------------------+
        | Predict Fruit/Vegetable |
        +------------------------+
```

---

## 🧾 Project Files

```
Image_classification/
├── app.py                  # Flask API server
├── Image_Class_Model.ipynb # Jupyter notebook for training the CNN model
├── model.h5                # Saved Keras model (optional)
├── test_images/            # Sample images to test classification
├── static/                 # Flask static folder (for UI assets, if needed)
├── templates/              # Flask templates folder (for web UI)
├── requirements.txt        # Python dependencies
```

---

## 🔍 Model Details

* **Framework**: TensorFlow / Keras
* **Model Type**: CNN
* **Layers**: Conv2D, MaxPooling2D, Flatten, Dense
* **Activation**: ReLU, Softmax
* **Loss Function**: Categorical Crossentropy
* **Optimizer**: Adam

Training was done on a dataset containing labeled images of fruits and vegetables split into training and validation sets.

---

## 🚀 How to Run the Project

### 🔧 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 🧠 2. (Optional) Train the Model

If not using the pre-trained model:

```bash
jupyter notebook Image_Class_Model.ipynb
```

Export the trained model as `model.h5`

### 🌐 3. Run the Flask Server

```bash
python app.py
```

Visit: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## 🧪 API Usage

The Flask app exposes a web form to upload an image. It predicts the class and displays the result on the webpage.

Alternatively, you can send a POST request to the `/predict` endpoint with an image file using Postman or `curl`.

### Example `curl` request:

```bash
curl -X POST -F image=@path_to_image.jpg http://127.0.0.1:5000/predict
```

---

## 🧾 Requirements

```
flask
tensorflow
keras
numpy
pillow
```

---

## 📈 Future Improvements

* Add model accuracy and loss graphs on the web interface
* Support more categories and real-time camera input
* Deploy on cloud (Heroku, Render, etc.)

---

## 👨‍💻 Author

**Dimpu Nithish Karanam**
Image Classification | Deep Learning | Web Deployment
