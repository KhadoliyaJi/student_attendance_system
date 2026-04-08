# Face Recognition Attendance System

This project is a real-time face recognition-based attendance system developed using Dlib and OpenCV. It detects and recognizes faces using deep learning-based embeddings and automatically records attendance in a database.

---

## Features

* Real-time face detection using webcam
* Face recognition using 128-dimensional embeddings
* 68 facial landmark detection for accurate face alignment
* Automatic attendance marking with date and time
* Attendance stored in SQLite database
* GUI-based face registration system
* Efficient matching using Euclidean distance

---

## Technologies Used

* Python
* Dlib
* OpenCV
* NumPy
* Pandas
* Tkinter
* SQLite

---

## Working of the System

1. Face Registration
   The system captures multiple images of each user through the webcam and stores them locally.

2. Feature Extraction
   Facial landmarks (68 points) are detected and a 128-dimensional feature vector is generated for each face.

3. Face Recognition
   The system captures live video, detects faces, and compares them with stored features using Euclidean distance.

4. Attendance Marking
   When a match is found, the system records the name, time, and date in the database. Duplicate entries for the same day are prevented.

---

## Project Structure

```
face_recognition_system/
│
├── Face_recognition_system/
│   ├── app.py
│   ├── getting_face_from_camera.py
│   ├── feature_extraction_to_csv.py
│   ├── attendence_taker.py
│   ├── templates/
│   │   └── index.html
│   └── requirements.txt
│
├── data/
│   ├── data_dlib/
│       ├── dlib_face_recognition_resnet_model_v1.dat
|       └── shape_predictor_68_face_landmarks.dat
|   └── data_faces_from_camera
│
├── README.md
└── .gitignore
```

---

## Installation and Setup

### 1. Clone the repository

```
git clone https://github.com/KhadoliyaJi/student_attendance_system.git
cd student_attendance_system
```

---

### 2. Install dependencies

```
pip install -r Face_recognition_system/requirements.txt
```

---

### 3. Download Required Models

Download the required model files from:

https://drive.google.com/drive/folders/13oZUcf3055X38sjQBBOeNwkrYFXdT2JG?usp=sharing

Place them inside:

```
data/data_dlib/
```

---

### 4. Run the project

Step 1: Register faces

```
python getting_face_from_camera.py
```

Step 2: Extract features

```
python feature_extraction_to_csv.py
```

Step 3: Start attendance system

```
python attendence_taker.py
```

---

## Database

The system uses an SQLite database (`attendance.db`) to store:

* Name
* Time
* Date

Each student’s attendance is recorded only once per day.

---

## Key Concepts

* Face Detection
* Facial Landmark Detection (68 points)
* Face Embeddings (128-dimensional vectors)
* Euclidean Distance
* Real-time video processing

---

## Future Improvements

* Web-based dashboard for attendance
* Improved accuracy using advanced models
* Multi-user and multi-camera support
* Deployment as a web application

---

## Author

Rahul Khadoliya
B.Tech Computer Science Engineering

---

## Note

Model files and datasets are not included in the repository due to their large size. Please download them separately using the provided link.
