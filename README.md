# Predictive Model for Traffic Management  Using ML
## Overview
This project develops a web-based traffic analysis and prediction system built with Flask, YOLOv8, and supporting libraries. The application processes live video streams to detect and count vehicles in real time, and leverages a pre-trained machine learning model to predict traffic conditions based on the collected vehicle data.

## 🚦 Features
- **Real-time Vehicle Detection & Counting**: Detects cars, buses, and trucks using YOLOv8.  
- **YouTube Live Stream Integration**: Supports live video feeds as input.  
- **Interactive Map Visualization**: Choropleth maps for visualizing traffic data using Plotly.  
- **Predictive Analytics**: Uses a pre-trained ML model to forecast traffic conditions.  

---

## 🛠 Technologies Used
- **Flask** → Web framework for backend and routing.  
- **YOLOv8** → State-of-the-art object detection for vehicles.  
- **Plotly** → Interactive and dynamic map visualizations.  
- **scikit-learn** → Preprocessing and machine learning for prediction.  
- **OpenCV** → Video frame extraction and processing.  
- **yt-dlp / pytube** → Fetching YouTube live stream URLs.  

---

## ⚙️ Installation  

1. **Clone the repository**  
   ```bash
   git clone https://github.com/shreya-1x1/YOLOv8-Traffic-Analysis
   cd YOLOv8-Traffic-Analysis
   
2. Create a virtual environment:
   ```bash
   python -m venv venv
   venv\Scripts\activate
   ```
   
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Ensure the YOLOv8 model weights are present:
   The YOLOv8 model weights are already included in the `yolov8/` directory of this repository.

5. Ensure the required GeoJSON file is present:
   Ensure the GeoJSON file is in the `data/` directory.

6. Ensure you have the pre-trained machine learning model file:
   Place the model file (`model.joblib`) in the project directory.

7. Train the Random Forest Classifier (Optional):
   The Jupyter Notebook file included in the repository is used to train a Random Forest Classifier. The trained model is saved as `model.joblib` and is utilized by `app_realtime.py` for predictions.


## Usage

1. Run the Flask application:
   ```bash
   python app_realtime.py
   ```

2. Open the application in your web browser:
   Navigate to `http://127.0.0.1:5000`.

3. Select a live video stream and view real-time traffic analysis and predictions.

## File Structure
```
.
├── app_realtime.py                                     # Main Flask application
├── data
│   └── map.geojson                                     # GeoJSON file for map visualization
│   └── Traffic.csv                                     # Dataset used to train model
├── model.joblib                                        # Trained ML model
├── requirements.txt                                    # Python dependencies
├── templates
│   └── index.html                                      # HTML templates
├── traffic-prediction-detailed-eda-modeling.ipynb      # Jupyter Notebook used to train model
├── yolov8
    ├── coco.txt                                        # Class labels for YOLO
    ├── tracker.py                                      # Tracks Boundary Boxes across frames
    └── yolov8s.pt                                      # YOLOv8 model weights
```


## 🚀 Future Enhancements
- Add support for multiple machine learning models for traffic prediction.  
- Improve vehicle detection accuracy using advanced YOLO configurations.  
- Integrate additional live video stream sources.  
- Enhance the user interface for a smoother and more intuitive experience.  

## 🤝 Contributing
Feel free to fork the repository, create a feature branch, and submit a pull request.


## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


