# YOLOVision

YOLOVision is a simple object detection project using the YOLOv8 model. It utilizes the `ultralytics` library for YOLO implementation and OpenCV for real-time video processing. The project detects objects from a live webcam feed and displays bounding boxes, class names, and confidence scores on the screen.

## Features
- Real-time object detection using YOLOv8.
- Displays bounding boxes, class names, and confidence scores for detected objects.
- Simple and lightweight implementation using Python.

---

## Requirements

- Python 3.8 or higher
- OpenCV
- Ultralytics YOLO library

Install the required packages using pip:
```bash
pip install opencv-python ultralytics
```

---

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/YOLOVision.git
   cd YOLOVision
   ```

2. Download YOLOv8 model weights:
   - Download `yolov8n.pt` (nano model) from the [Ultralytics YOLOv8 models page](https://github.com/ultralytics/ultralytics#models) or directly using the script:
     ```bash
     wget https://github.com/ultralytics/assets/releases/download/v0.0.0/yolov8n.pt
     ```
   - Save it in the `yolo-Weights` directory.

3. Run the script:
   ```bash
   python yolovision.py
   ```

---

## Code Explanation

### Main Components:
1. **Model Initialization**:
   ```python
   model = YOLO("yolo-Weights/yolov8n.pt")
   ```
   Loads the YOLOv8 model for inference.

2. **Video Capture**:
   ```python
   capture = cv2.VideoCapture(0)
   ```
   Captures the live video feed from your default webcam.

3. **Object Detection Loop**:
   - Processes each frame to detect objects.
   - Draws bounding boxes, displays class names, and shows confidence levels for each detected object.

4. **Output Display**:
   ```python
   cv2.imshow('Webcam', img)
   ```
   Displays the processed video feed with annotations in real time.

---

## How to Use
1. Connect a webcam to your computer.
2. Run the script.
3. The live video feed will open in a window. Detected objects will be highlighted with bounding boxes, and their names and confidence scores will be displayed.
4. Press `q` to exit the application.

---

## Example Output

The script will show the detected objects like this:

- **Bounding Boxes**: Around detected objects.
- **Class Names**: Labels for objects like `person`, `car`, etc.
- **Confidence Scores**: Probabilities of detection.

---


## License

This project is licensed under the [MIT License](LICENSE).

---

## Acknowledgments
- [Ultralytics YOLO](https://github.com/ultralytics/ultralytics) for the YOLO library.
- [OpenCV](https://opencv.org/) for real-time computer vision tools.

Feel free to contribute to YOLOVision by submitting pull requests or opening issues!
