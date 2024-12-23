
# TrafficVision: AI-Powered Traffic Timing

TrafficVision is an AI-powered system designed to optimize traffic signal timings in real-time. It uses Faster R-CNN for object detection and Linear Regression for prediction, adjusting signal timings based on current traffic density to enhance flow and reduce congestion. The project also incorporates ESP8266 and ESP32-CAM for data collection and real-time traffic monitoring.

## Features

- **Real-time Traffic Detection**: Faster R-CNN detects and counts vehicles at intersections.
- **Adaptive Signal Timings**: Adjusts signal timings based on predicted traffic density.
- **Flask API**: Accessible through RESTful API endpoints.
- **Edge Compatibility**: ESP8266 and ESP32-CAM facilitate traffic monitoring and data capture.

## Table of Contents

1. [Installation](#installation)
2. [Dependencies](#dependencies)
3. [Usage](#usage)
4. [Models Used](#models-used)
5. [Hardware Requirements](#hardware-requirements)
6. [Results](#results)
7. [Future Improvements](#future-improvements)
8. [Contributing](#contributing)
9. [License](#license)

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/dhnz-2006/TrafficVision.git
   cd TrafficVision
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Download Dataset**: Ensure you have a dataset of annotated traffic images to train and test the Faster R-CNN model.

4. **Set Up Hardware**:
   - Connect the ESP32-CAM to capture live traffic images.
   - Configure ESP8266 to transmit captured images to the Flask server.

## Dependencies

TrafficVision relies on the following dependencies, which are listed in `requirements.txt`:

- **Flask**: For creating the API server.
- **PyTorch**: For Faster R-CNN model implementation.
- **OpenCV**: For image processing.
- **Requests**: For handling HTTP requests.

Install all dependencies using:

```bash
pip install -r requirements.txt
```

## Usage

1. **Start the Flask App**:
   Run the Flask server to handle incoming requests:
   ```bash
   python app.py
   ```

2. **Use API Endpoints**:
   - **POST /predict**: Accepts traffic images as input and returns predicted signal timings.
   
   You can test the API locally by sending a request with a sample traffic image.

## Models Used

1. **Faster R-CNN for Object Detection**: Detects and counts vehicles.
2. **Linear Regression for Signal Prediction**: Forecasts traffic density and suggests optimal timings.

## Hardware Requirements

- **ESP8266**: Manages data communication with the server.
- **ESP32-CAM**: Captures live traffic footage and sends images to the Flask server for analysis.

## Results

TrafficVision accurately detects vehicles and adjusts signal timings. Results, including vehicle counts and timing recommendations, are available through API responses and can be viewed in real-time.

## Future Improvements

- **Optimized Detection Models**: Explore YOLO or SSD for faster detection.
- **Deep Learning Prediction Models**: Improve signal timing predictions using more advanced neural networks.
- **Edge Deployment**: Optimize model for low-power devices like Raspberry Pi.

## Contributing

We welcome contributions! Fork the repository, create a feature branch, and submit a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
