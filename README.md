# 🔍 Real-Time Face Detection with Webcam

🎯 **Project Description**  
This is a simple real-time face detection app that uses your webcam to detect faces through a browser interface. It combines **Python (OpenCV)** for face detection and **JavaScript** for accessing the webcam and displaying results in the browser.

---

## 🧰 Technologies Used

- **Python** – For image processing and server logic.
- **OpenCV** – To detect faces in real-time using the webcam.
- **JavaScript** – To access the user's webcam and send video frames.
- **Flask** – To build the backend server in Python.
- **Anaconda** – For managing the Python environment.

---

## 📸 How It Works

1. **Access webcam in browser (via JavaScript)**  
   JavaScript uses `getUserMedia()` to access and display the webcam stream.

2. **Capture video frames**  
   A frame is captured every second and sent to the backend using a POST request.

3. **Face detection with OpenCV**  
   Flask receives the frame and uses OpenCV with Haar Cascade classifiers to detect faces.

4. **Send back the result**  
   The image with face rectangles drawn on it is returned and displayed in the browser.

---

## How to Use

### 1.Open the project in your browser (localhost:5000).
### 2.Allow access to the webcam.
### 3.The webcam feed will appear in real-time.
### 4.The browser captures a frame every second and sends it to the server.
### 5.The server detects faces and returns the processed image.
### 6.The result (with face boxes) is displayed on the web page.

---
## 📁 Project Structure

face-detection/
│
├── static/
│   └── script.js                      # JavaScript for webcam and frame sending
│
├── templates/
│   └── index.html                     # Front-end HTML page
│
├── app.py                             # Flask backend with face detection logic
├── haarcascade_frontalface_default.xml  # Pretrained face detection model (Haar Cascade)
├── requirements.txt                   # List of Python dependencies
└── README.md                          # Project documentation (you are reading it)
