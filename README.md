# Mobility Aid for the Visually Impaired

### About the project
This project was developed for the in house Summer Internship at Amity University Mumbai with the main objective of helping the visually impaired to better navigate their surroundings by using sensors to alert them about obstacles in their path and a mounted camera for object detection.

### Built With
* Arduino Uno
* HC-SR04 Ultrasonic Module
* Vibration Motor
* Camera

### Object Detection
For the object detection model me and my team used the **YOLO algorithm** because of its speed and accuracy. YOLO is an abbreviation for the term *‘You Only Look Once’*. This is an algorithm that detects and recognizes various objects in a picture (in real-time). Object detection in YOLO is done as a regression problem and provides the class probabilities of the detected images.

It works by dividing the screen into regions and locate a particular object acordingly. We're using **yolov3 with Voice Feedback using gTTS** so the output is in voice format.

**Example:** If a bottle is held straight in front of the camera then the output will be *"mid center bottle"*.

Download the yolov3 weights from [here](https://pjreddie.com/media/files/yolov3.weights)

### Obstacle Detection
For determining how far the obstacles are from the user we use four **Ultrasonic sensors** strapped to the arms and legs of the user. 

It works by emitting an ultrasound at 40 kHz from the transmitter which travels through the air and if there is an obstacle in its path it will bounce back to the module and the reciever will catch it.
The ultrasonic module is paired with the **Arduino Microprocessor** which calculates the distance at which the obstacle is located using the travel time of the wave and the speed of sound.

For the feedback mechanism a vibrating motor is used to alert the user if there is an obstacle within 50cm.
