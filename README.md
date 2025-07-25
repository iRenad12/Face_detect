
## 🔍 Face Detection Project using OpenCV

### 📌 Project Overview
This project demonstrates a simple real-time **face detection** system using Python and OpenCV. It utilizes the **Haar Cascade Classifier** (`haarcascade_frontalface_default.xml`) to detect human faces in images captured from a webcam.

---

### 💡 Features
- Detects one or multiple faces in real-time using your webcam.
- Draws rectangles around detected faces.
- Displays the video feed with face highlights in a window.

---

### 🧠 How It Works
1. **OpenCV Initialization**: The script starts by importing OpenCV (`cv2`) for computer vision operations.
2. **Cascade Classifier Loading**: The face detection model is loaded from `haarcascade_frontalface_default.xml`, which contains pre-trained data for frontal face recognition using the Haar feature-based cascade classifier.
3. **Webcam Access**: It opens the default camera using `cv2.VideoCapture(0)`.
4. **Frame Reading Loop**:
   - Captures each frame from the camera.
   - Converts it to grayscale (since Haar cascades work better on grayscale images).
   - Runs face detection on the grayscale frame using `detectMultiScale()`.
   - For each detected face, draws a green rectangle around it.
   - Displays the frame in a window titled `"frame"`.
5. **Exit**: When the user presses `q`, the loop ends, the camera is released, and all OpenCV windows are closed.

---

### 📁 File Structure
```
├── face1_detect.py                     # Main script for face detection
├── haarcascade_frontalface_default.xml # Haar cascade classifier data file
```

---

### 🛠️ Requirements
- Python 3.x
- OpenCV (`cv2`)

You can install OpenCV using pip:
```bash
pip install opencv-python
```

---

### ▶️ How to Run
Make sure both `face1_detect.py` and `haarcascade_frontalface_default.xml` are in the same directory.

Then run:
```bash
python face1_detect.py
```

Press `q` to exit the video feed window.

---

### 📸 Sample Output
- Real-time webcam feed with green boxes around detected faces.

---

### ✅ Use Cases
- Basic facial detection for learning computer vision.
- Can be extended to emotion detection, face recognition, attendance systems, etc.

---

### 📌 Notes
- Ensure the lighting is good for better face detection accuracy.
- Haar cascades work well for frontal faces but may miss side or occluded faces.
