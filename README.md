# Attendify 🎯

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![Python](https://img.shields.io/badge/Python-3.7%2B-blue.svg)](https://www.python.org/downloads/)
[![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-red.svg)](https://opencv.org/)

## 📋 Overview

**Attendify** is an intelligent facial recognition-based attendance system that automates the process of tracking attendance in real-time. The system uses advanced computer vision techniques to identify individuals through a webcam feed and automatically logs their attendance with timestamps to a CSV file.

## ✨ Key Features

- **Real-time Facial Recognition**: Utilizes OpenCV and face_recognition libraries for accurate face detection
- **Automated Attendance Logging**: Automatically records attendance with precise timestamps
- **User-Friendly Interface**: Simple webcam-based interface with visual feedback
- **Duplicate Prevention**: Prevents multiple entries for the same person in a single session
- **CSV Data Export**: Exports attendance records in a structured CSV format for easy analysis
- **Live Visual Feedback**: Displays recognized names with bounding boxes around detected faces

## 🛠️ Technical Architecture

### Core Technologies
- **Python 3.7+**: Primary programming language
- **OpenCV**: Computer vision and image processing
- **face_recognition**: Facial detection and encoding
- **NumPy**: Numerical computations and array operations
- **CSV**: Data storage and export functionality

### System Workflow
1. **Image Loading**: Loads reference images from the `ImagesAttendance` directory
2. **Face Encoding**: Generates unique facial encodings for each reference image
3. **Real-time Detection**: Captures live video feed and detects faces in each frame
4. **Face Matching**: Compares detected faces with stored encodings using distance algorithms
5. **Attendance Logging**: Records attendance data with timestamps to `Attendance.csv`

## 🚀 Installation & Setup

### Prerequisites
```bash
# Install required dependencies
pip install opencv-python
pip install face-recognition
pip install numpy
```

### Installation Steps
1. **Clone the Repository**
   ```bash
   git clone https://github.com/Ayush-Mann-0/Attendify.git
   cd Attendify
   ```

2. **Prepare Reference Images**
   - Add individual photos to the `ImagesAttendance/` directory
   - Name files with the person's name (e.g., `john_doe.jpg`)
   - Ensure clear, front-facing photos for optimal recognition

3. **Run the Application**
   ```bash
   python main.py
   ```

## 📁 Project Structure

```
Attendify/
├── main.py                    # Core application logic
├── Attendance.csv             # Attendance records (auto-generated)
├── ImagesAttendance/          # Directory for reference photos
│   └── placeYourImagesHere.txt
├── LICENSE                    # MIT License
└── README.md                  # Project documentation
```

## 💡 Usage Instructions

1. **Setup Phase**:
   - Place clear, front-facing photos in the `ImagesAttendance/` folder
   - Ensure filenames match the names you want to appear in attendance records

2. **Operation**:
   - Execute `python main.py` to start the system
   - Position yourself in front of the webcam
   - The system will automatically detect and log your attendance
   - Press any key to exit the application

3. **Data Access**:
   - View attendance records in the auto-generated `Attendance.csv` file
   - Data includes names and precise timestamps

## 🎯 Technical Highlights

- **Advanced Face Recognition**: Implements state-of-the-art facial recognition algorithms
- **Real-time Processing**: Optimized for live video processing with minimal latency
- **Scalable Architecture**: Easily accommodates additional users by adding reference images
- **Data Integrity**: Prevents duplicate entries and ensures accurate timestamp logging
- **Cross-platform Compatibility**: Runs on Windows, macOS, and Linux systems

## 🔧 Configuration Options

- **Video Source**: Modify `cv2.VideoCapture(0)` to change camera input
- **Image Scaling**: Adjust resize parameters for performance optimization
- **Recognition Threshold**: Fine-tune face distance thresholds for accuracy
- **Output Format**: Customize CSV output structure as needed

## 📊 Applications

- **Educational Institutions**: Automated classroom attendance
- **Corporate Offices**: Employee check-in systems
- **Event Management**: Participant tracking for conferences and workshops
- **Security Systems**: Access control and monitoring
- **Time & Attendance**: Workforce management solutions

## 🤝 Contributing

Contributions are welcome! Please feel free to submit pull requests, report issues, or suggest enhancements.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Developer

**Ayush Mann** - [GitHub Profile](https://github.com/Ayush-Mann-0)

---

*Developed with ❤️ using Python and Computer Vision technologies*
