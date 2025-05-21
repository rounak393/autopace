# autopace
# 🚗 Traffic Speed Detection with YOLOv8(assosciated with IDEAS@-ISI KOLKATA)

This project uses [YOLOv8](https://github.com/ultralytics/ultralytics) for vehicle detection and calculates their speed based on frame analysis in a traffic video. Ideal for smart city applications, traffic monitoring, and basic computer vision tasks.

## 📌 Features

- Detects vehicles in traffic videos using YOLOv8
- Calculates vehicle speed in km/h based on virtual line crossing
- Supports `.mp4`, `.avi`, and other common video formats
- Automatically resizes large videos to 720p for performance
- Annotated output video with speed overlay and bounding boxes

## 🔧 Requirements

This notebook is designed to run in **Google Colab**. It uses the following libraries:

- Python 3.9+
- [Ultralytics](https://github.com/ultralytics/ultralytics)
- OpenCV
- PyTorch

## 🚀 Setup and Usage

1. **Open in Google Colab**  
   Upload the notebook and run it in a Colab environment.

2. **Install dependencies** (already included in the notebook):
   ```bash
   !pip install ultralytics opencv-python
3.Upload your video
The notebook will prompt you to upload a .mp4, .avi, or similar video.

4.Run the detection and speed calculation
The script:

Loads the YOLOv8n model

Processes each frame

Tracks vehicles crossing a virtual line

Calculates speed using the formula:

Speed (km/h)
=
Distance (m)
Time (s)
×
3.6
Speed (km/h)= 
Time (s)
Distance (m)
​
 ×3.6
5.Download your output
Once processing is complete, a processed video with overlaid speeds and bounding boxes will be available for download.
![autopace1](https://github.com/user-attachments/assets/f8a1e588-9ef1-413d-b266-00467f74ea74)
![autopace2](https://github.com/user-attachments/assets/9e91b5b0-717f-496a-a263-40110908520f)



6.⚙️ Configuration
real_distance_m: Real-world distance (in meters) between the two virtual line points. Default is 10.

resize_width, resize_height: Resize dimensions to optimize processing. Default is 1280x720.

line_y: The y-coordinate of the imaginary line used for speed measurement.

7.📁 Output
speed_processed_video.mp4: Output video with vehicle detections and speed annotations.



8.🧠 Model Info
Model: YOLOv8n (yolov8n.pt) – lightweight and fast

Detection class: Only detects cars (class == 2) with confidence > 0.4

9.📝 Notes
This approach assumes a fixed camera angle and constant vehicle direction across the frame.

For more precise results, calibration with real-world measurements is recommended
