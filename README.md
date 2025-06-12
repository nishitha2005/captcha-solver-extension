# captcha-solver-extension
# Overview  
CAPTCHA Solver is a **deep learning-powered** browser extension that automates the solving of alphanumeric CAPTCHAs using **YOLO** for character detection and a **CNN** for character recognition.  

This project aims to enhance accessibility and user experience by **automatically detecting and solving CAPTCHA challenges** on websites, saving users time and effort. 

# ARCHITECTURE
The backend is built with Node.js and Express.js, providing API endpoints to receive CAPTCHA images for processing.
Upon receiving an image, the backend forwards it to the deep learning module for analysis.
The deep learning module uses the YOLO model to perform real-time object detection, accurately segmenting individual characters from the CAPTCHA image.
After segmentation, each detected character is passed to a k (CNN) for classification.
The custom CNN is designed and trained using PyTorch to achieve high precision in character recognition despite distortions and noise.
The project also includes a React.js-based playground that allows users to generate and interact with CAPTCHAs in a controlled environment.
The extension sends the captured image to the backend, triggering the automated solving process.
Once the CAPTCHA is solved by the deep learning models, the decoded text is automatically populated into the input fields on the web page.

# YOLO and CNN Performance Metrics
YOLO Model was trained for 50 epochs, achieving a precision of 97.3% and a recall of 95.9% for character detection.
CNN Model was trained for 20 epochs, achieving a validation accuracy of 98.67%, outperforming traditional CNNs.

## Demo Video
[Click here to watch the demo](https://drive.google.com/file/d/1HcE60CTV0bGbzw_WbpFrJ8CQ9C-g5CRl/view?usp=drive_link)
