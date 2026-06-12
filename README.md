# 🚦 Smart Traffic Management System using YOLOv5

## 📌 Overview

The Smart Traffic Management System is an AI-powered traffic optimization solution that uses Computer Vision and YOLOv5 object detection to analyze traffic density and dynamically allocate traffic signal timings.

The system detects vehicles from uploaded traffic images, counts different vehicle types, and calculates optimal green signal durations based on vehicle density, helping reduce congestion and improve traffic flow.

---

## ✨ Features

- Vehicle detection using YOLOv5
- Automatic vehicle counting
- Dynamic traffic signal timing calculation
- Detection of:
  - Cars
  - Buses
  - Trucks
  - Motorcycles
  - Bicycles
- ZIP file upload support
- Annotated output images with bounding boxes
- Automatic signal timing report generation
- Supports multiple traffic lanes

---

## 🎯 Problem Statement

Traditional traffic signals operate on fixed timing schedules, often leading to unnecessary delays and traffic congestion.

This project aims to optimize traffic flow by dynamically calculating traffic signal timings based on the actual number and type of vehicles present at an intersection.

---

## 🏗️ System Workflow

1. Upload a ZIP file containing traffic images.
2. Extract images automatically.
3. Detect vehicles using YOLOv5.
4. Count vehicles in each lane.
5. Calculate traffic density.
6. Generate Green, Yellow, and Red signal timings.
7. Save annotated output images.
8. Generate signal timing reports.

---

## 🛠️ Technologies Used

- Python
- YOLOv5
- PyTorch
- OpenCV
- Google Colab
- NumPy

---

## 📊 Dataset

The project uses a pretrained YOLOv5s model trained on the COCO Dataset.

### COCO Dataset

- Approximate Size: 118,000+ training images
- Object Classes: 80
- Vehicle Classes Used:
  - Car
  - Bus
  - Truck
  - Motorcycle
  - Bicycle

Custom traffic images are used as test inputs during execution.

---

## 🚗 Vehicle Detection Classes

The system detects:

- Car
- Bus
- Truck
- Motorcycle
- Bicycle

---

## ⏱️ Traffic Signal Timing Logic

Green signal duration is calculated using:

- Number of detected vehicles
- Average crossing time of each vehicle type
- Number of traffic lanes

### Constraints

| Parameter | Value |
|------------|---------|
| Minimum Green Time | 10 sec |
| Maximum Green Time | 60 sec |
| Yellow Time | 5 sec |

---

## 📁 Project Structure

```text
Smart-Traffic-Management/
│
├── test_images/
│
├── output_images/
│
├── signal_times.txt
│
├── smart_traffic_management.py
│
└── README.md
```

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/Sri-Vardhan-git/YOUR_REPOSITORY_NAME.git
cd YOUR_REPOSITORY_NAME
```

### Install Dependencies

```bash
pip install torch torchvision
pip install opencv-python
pip install ultralytics
```

---

## ▶️ Usage

### Step 1

Upload a ZIP file containing traffic images.

Example:

```text
traffic_images.zip
│
├── lane1.jpg
├── lane2.jpg
├── lane3.jpg
└── lane4.jpg
```

### Step 2

Run the Python script.

```bash
python smart_traffic_management.py
```

### Step 3

View results in:

```text
output_images/
signal_times.txt
```

---

## 📈 Sample Output

```text
Detected Vehicles:
Car: 12
Bus: 2
Truck: 1
Motorcycle: 8
Bicycle: 3

Green Time : 25 sec
Red Time   : 35 sec
Yellow Time: 5 sec
```

---

## ✅ Results

- Accurate vehicle detection using YOLOv5.
- Dynamic traffic signal timing allocation.
- Reduced dependency on fixed-time traffic control.
- Improved traffic density analysis and decision-making.

---

## 🚀 Future Enhancements

- Real-time CCTV integration
- Live video stream processing
- Emergency vehicle prioritization
- Multi-intersection traffic coordination
- IoT-enabled traffic control
- Cloud dashboard for monitoring

---

## 🌍 Applications

- Smart Cities
- Urban Traffic Management
- Intelligent Transportation Systems
- Traffic Congestion Reduction
- Highway Monitoring

---

## 👨‍💻 Author

**Sri Vardhan**

GitHub: https://github.com/Sri-Vardhan-git

---

## 📄 License

This project is developed for educational and research purposes.
