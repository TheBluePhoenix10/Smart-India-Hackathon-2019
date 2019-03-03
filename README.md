# Smart-India-Hackathon-2019
Driver alertness and rash driving detection

This repository consists of different files and data for driver alertness system
We have implemented different features to provide alertness to the driver at the time of driving
This solution addresses seven different user cases in order to provide better feedback to the driver which will help in reducing the number of accidents

Features:
1) Drowsiness detection
2) Alcohol detection
3) Emotion analysis and detection
4) Lane detection
5) Proximity sensing and audio alert(in different languages)
6) Traffic sign detection 
7) Distraction by the use of mobile

Drowsiness detection:
We are detecting Eye Aspect Ratio(EAR) using Haar cascade classifier along with Adaboost optimizer which is the world's finest optimizer binary classification, unlike other approaches which only use Haar cascade.

Alcohol detection
The system uses MQ3 sensor and STM 32 to detect alcohol vapours in the driver's breath. An external switch is connected to control the motion of the servo motor. Servo motor is used to represent engine system in our prototype. When alcohol amount greater than the legal limit is detected, the car won't start and the driver will get an LED indication.
 
Emotion Analysis and detection:
If the driver is angry and hence it’s not safe for him to drive, An SMS alert will be sent to his Guardian/Emergency contact, The Guardian/Emergency contact can start a video call with the driver using the Front cam installed inside the car. The driver would be able to listen to voice of the person using speaker and communicate using mic.

Lane detection:
The system uses sobel and gradient filters for detection of the lines. Radius of curvature value is used to decide the threshold. Sliding window is used to detect lane changes, we are using three colour scheme to detect the rash driving cases,
Green- Normal driving
Blue- Threshold crossed once
Red- If the threshold is crossed continuously for next 50 frames- In this case we will send some alert signal.

Proximity sensing and audio alert:
This feature will keep the driver alert about the distance with objects and other cars avoiding crashes. It will give different audio warnings to the driver whenever a vehicle or pedestrian is detected in close vicinity. The audio output is available in different languages and the driver has a choice to select a language as per his preference.

Traffic sign detection:
Traffic signs are sometimes ignored when driver isn't paying attention, this feature gives audio warning to the driver whenever any important traffic sign is detected.

Distraction by the use of mobile:
EAR is used to implement this technique. if the driver is on his/her phone for a long time then the system sets off a buzzer sound which alerts the driver.




