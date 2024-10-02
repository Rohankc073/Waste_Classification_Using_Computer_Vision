
### **Waste Classification Using Computer Vision**

This project uses Convolutional Neural Networks (CNN) to classify waste into two categories: Organic and Recyclable. The AI-driven system, leveraging image processing techniques, is designed to improve waste management efficiency. The solution has been tailored for low-resource environments like Nepal, where waste segregation plays a crucial role in environmental sustainability.

### **Project Overview**

This project automates waste classification using a CNN model to analyze images captured from a webcam. The model categorizes the waste as BIODEGRADABLE (organic) or RECYCLABLE and sends control signals to an external Arduino for appropriate action based on the classification.

### **Key Features**
- Real-time image capture using a webcam.
- Zoom functionality to enhance captured image quality for classification.
- Integration with Roboflow API for waste classification.
- Serial communication with Arduino to control external devices based on waste type.
- Robust retry mechanism for handling network-related issues.

### **Technologies Used**
- **Python**: The primary programming language for building the system.
- **OpenCV**: For image processing and video capture.
- **Roboflow API**: For classifying waste into categories.
- **Convolutional Neural Networks (CNN)**: Used for image-based waste classification.
- **Serial communication**: For interfacing with Arduino to send signals based on waste classification.
- **Matplotlib**: For visualizing the live video feed.

### **Hardware Structure**
The system includes the following hardware components:
- **1 x USB Camera**: Used for capturing real-time waste images.
- **2 x Waste Bins**: One for biodegradable waste and one for recyclable waste.
- **2 x Servo Motors (25 KG)**: Responsible for moving and segregating waste into the appropriate bin.
- **1 x Arduino UNO Board**: Central controller that receives classification signals and controls the motors.
- **1 x Buck Module (Step-Down) 5V**: Converts voltage for powering the components.
- **1 x 12V Battery**: Power source for the system.

### **Project Flow**
1. Capture an image from a webcam.
2. Apply zoom to the captured frame.
3. Save the image and send it to the Roboflow API for classification.
4. Based on the classification (organic or recyclable), send appropriate signals to an Arduino.
5. Continuously update the counts for organic and recyclable waste, and display these on the screen.

### **How it Works**
The system captures an image of waste, processes it, and sends it to the Roboflow API using HTTP requests. The API returns predictions about the waste type (organic or recyclable). The system then sends signals to an Arduino to perform different actions based on the waste type (e.g., segregating waste). The counts for each type of waste are updated and displayed in real-time.

---
