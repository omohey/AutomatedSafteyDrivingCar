# Automated Safety Driving Car

## Presented By

| Name | Github |
| :---: | :---:  |
| Mazen Hassan   | [mhassan20328](https://github.com/mhassan20328) |
| Kareem Amr     |   
| Omar Mohamed   |   [OmarMoheyeldinMohamed](https://github.com/OmarMoheyeldinMohamed) |
| Ahmed Dardir   |   [ahesham900](https://github.com/ahesham900)


## Presented To & Supervised By:

Dr Mohamed Shalan

## [Github Repo](https://github.com/OmarMoheyeldinMohamed/AutomatedSafteyDrivingCar)

## Problem Statement

"According to the World Health Organization (WHO), over 1.35 Millions are killed each year due to traffic accidents, these accidents stem from the human errors and lack of following traffic rules. There are trials to increase the safety procedures by automated systems that capitalizes on cameras but this can be brought to failure due to the poor vision and conditions that affect the camera and its efficiency. Consequently, different reliable systems are approached to handle this problem in a safer way.

## Background & Motivation

With the aforementioned numbers regarding death tolls due to traffic accidents, These traffic accidents are largely dependent on and caused by the lack of abiding by traffic rules. Hence, with the increase of demand on embedded systems especially in the automotive industry, we got motivated to explore more about the industry based on what we learned in the course so far as well as the lab to develop a model categorized Partial autonomous driving systems that can increase safety features for a self driving car. 

## The Proposed Solution 

This project aims to support partial autonomous driving safety procedures to ensure the car abides by the traffic rules and road conditions. The system will use the line followers to make sure that the wheels will not cross the 2 lanes the car is navigating in between. There will be another safety feature to measure distance between the car and any abject in front it in order to detect it and stop the car accordingly. Hence, this increases safety and alarming conditions to the self driving car which can be incorporated later on a larger scope in a real time system. 

## The initial design
![Initial Design](https://i.postimg.cc/3WMLtppd/bdiagram.png)
## Identified components:
| Hardware Components | Image |
| :---: | :---: |
| [STM32L432KC Microcontroller](https://www.st.com/en/microcontrollers-microprocessors/stm32l432kc.html) | ![STM Microcontroller](https://i.postimg.cc/MGbvH8t4/STM.jpg) |
|ESP32-Cam|![2-4-removebg-preview](https://user-images.githubusercontent.com/66432580/235498482-5766401c-70d7-4645-93e0-ec59ab4ba62f.png) | [click here](https://store.fut-electronics.com/collections/camera/products/esp32-cam-development-board-with-camera)|
| [Parallax 28034 line follower](https://www.distrelec.biz/en/infrared-line-follower-kit-parallax-28034/p/17334743) | ![Parallax Line Follower](https://i.postimg.cc/sDvQcqDQ/Parallax.jpg) |
| [Ultrasonic Sensor HC-SR04](https://ram-e-shop.com/product/kit-ultrasonic-txrx/) | ![Ultrasonic Sensor](https://i.postimg.cc/wM3vwRH8/Ultrasonic.jpg) |
| [The Pololu TReX Motor Controller](https://www.pololu.com/product/777) | ![Polulu Controller](https://i.postimg.cc/Bvs2MpVr/polulu4.jpg) |
| [Dagu Wild Thumper 4WD Chassis](https://www.pololu.com/product/1567) | ![Dagu](https://i.postimg.cc/nrLsNw4W/Dagu.jpg) |
| [Jumper Wires](https://ram-e-shop.com/product/ph60-mf-20cm/) | ![Wires](https://i.postimg.cc/59PQ8b1W/Jumper-Wires.jpg) |
| [Bread Board](https://ram-e-shop.com/product/bb01-bread-board/) | ![Breadboard](https://i.postimg.cc/nr6D7Gmw/Breadboard2.jpg) |

## The First Milestone

* Integrating the ESP32 Camera and checking the presence of captured frames and video working on the web server 
* Integrating the Infrared sensors to try applying the lane detection
* Link For Demo: [Demo](https://drive.google.com/drive/folders/1-3KJ91FfxfCk9-20nycJq1BGQrZUv5BV)

## Next Steps

* Implement The Lane Detection Algorithm.
* Implement Image processing to handle the captured frames.
* Communicate with stm32 from esp32 camera to send instructions to the Dagu Microcontroller based on image processing.
* Implement the Ultrasonic Sensor to support object detection.
* Handle the testing for the whole system as well as verifying the real time functionality and requirements


