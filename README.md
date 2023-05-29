# Automated Safety Driving Car

## Presented By

|     Name     |                              Github                               |
| :----------: | :---------------------------------------------------------------: |
| Mazen Hassan |          [mhassan20328](https://github.com/mhassan20328)          |
|  Kareem Amr  |           [KareemAmr12](https://github.com/KareemAmr12)           |
| Omar Mohamed | [OmarMoheyeldinMohamed](https://github.com/OmarMoheyeldinMohamed) |
| Ahmed Dardir |            [ahesham900](https://github.com/ahesham900)            |

## Presented To & Supervised By:

Dr Mohamed Shalan

## [Github Repo](https://github.com/OmarMoheyeldinMohamed/AutomatedSafteyDrivingCar)

## Problem Statement

"According to the World Health Organization (WHO), over 1.35 Millions are killed each year due to traffic accidents, these accidents stem from the human errors and lack of following traffic rules. There are trials to increase the safety procedures by automated systems to help drivers abide by traffic rules. Consequently, partial autonomous reliable systems are approached to handle this problem in a safer way.

## Background & Motivation

With the aforementioned numbers regarding death tolls due to traffic accidents, These traffic accidents are largely dependent on and caused by the lack of abiding by traffic rules. Hence, with the increase of demand on embedded systems especially in the automotive industry, we got motivated to explore more about the industry based on what we learned in the course so far as well as the lab to develop a model categorized under Partial autonomous driving systems that can increase safety features for a self driving car and then investigate how it can be integrated to help humans later on.

## The Proposed Solution

This project aims to support partial autonomous driving safety procedures to ensure the car abides by the traffic rules and road conditions. The system will use the ESP-32 Camera with fish eye lens to make sure car will not cross the 2 lanes navigating in between. There will be another safety feature to measure distance between the car and any abject in front it in order to detect it and stop the car accordingly. It will also continue after the removal of the object in the right way between lanes. Hence, this increases safety and alarming conditions to the self driving car which can be incorporated later on a larger scope in a real time system.

## Features

- The car should navigate to follow a path between two lines.
- The car should stop whenever it detects an object infront of it.
- The car should continue moving again when the object moves from its path.

# Architecture

## Software Architecture

- For the STM32 Nucleo board: We decided to use STMCubeIDE for project management, source code editing, and program running.
- For the ESP32 CAM: We use Arduino IDE only to take a picture downsize it and send it to the STM32 Nucleo board.

## Hardware Architecture

### Block Diagram

![Block Diagram](https://i.postimg.cc/tCj8Ppdk/Block-Diagram.jpg)

### System Components

|                                               Component                                                |                                                                                                      Description                                                                                                       |                                                             Image                                                              | Estimated Price |
| :----------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------: | :-------------: |
| [STM32L432KC Microcontroller](https://www.st.com/en/microcontrollers-microprocessors/stm32l432kc.html) | It is the main controller of the system. It receives the image from the ESP32 CAM and processes it to detect the lines. Also communicates with the ultrasonic sensor to detect objects infront of the car and stop it. |                                 ![STM Microcontroller](https://i.postimg.cc/MGbvH8t4/STM.jpg)                                  |       $11       |
|          [ESP32-Cam](https://ram-e-shop.com/product/esp32-cam-development-board-with-camera/)          |                                           It is the camera of the system. When prompted by the STM32 Nucleo board it takes a picture and sends it to the STM32 Nucleo board.                                           | ![2-4-removebg-preview](https://user-images.githubusercontent.com/66432580/235498482-5766401c-70d7-4645-93e0-ec59ab4ba62f.png) |       $15       |
|            [Ultrasonic Sensor HC-SR04](https://ram-e-shop.com/product/kit-ultrasonic-txrx/)            |                                                                              It is used to detect objects infront of the car and stop it.                                                                              |                               ![Ultrasonic Sensor](https://i.postimg.cc/wM3vwRH8/Ultrasonic.jpg)                               |       $2        |
|                 [The Pololu TReX Motor Controller](https://www.pololu.com/product/777)                 |                                                                                      It is used to control the motors of the car.                                                                                      |                                ![Polulu Controller](https://i.postimg.cc/Bvs2MpVr/polulu4.jpg)                                 |      $200       |
|                  [Dagu Wild Thumper 4WD Chassis](https://www.pololu.com/product/1567)                  |                                                                                                 It is the car chassis.                                                                                                 |                                        ![Dagu](https://i.postimg.cc/nrLsNw4W/Dagu.jpg)                                         |      $350       |
|                      [Jumper Wires](https://ram-e-shop.com/product/ph60-mf-20cm/)                      |                                                                                        Used to connect the components together.                                                                                        |                                    ![Wires](https://i.postimg.cc/59PQ8b1W/Jumper-Wires.jpg)                                    |       $1        |
|                    [Bread Board](https://ram-e-shop.com/product/bb01-bread-board/)                     |                                                                                        Used to connect the components together.                                                                                        |                                  ![Breadboard](https://i.postimg.cc/nr6D7Gmw/Breadboard2.jpg)                                  |       $2        |

## Connections and Steps to Replicate the Project

### Folder Structure

- ESP32CameraSource folder contains all source files needed to program the ESP32 CAM.
- STMSource folder contains all source files needed to program the STM32 Nucleo board.

### Instructions

- Use the source code in the ESP32 CAM folder to program the ESP32 CAM.

* Open Arduino IDE and load the code into the camera. Note: you need to reset the camera anytime its power is cut off.

- Use the source code in the STM32 Nucleo board folder to program the STM32 Nucleo board. Note: you might want to use STMCubeMX to setup UART1 (setup baud rate at 19200), UART2 (setup baud rate to 230,400), and TIM1 (use a prescalar of 31 to achieve a 1us clock tick).
- Connect UART1 to the Pololu TReX Motor Controller.
- Connect UART2 to the ESP32 CAM.
- Connect the ultrasonic sensor trig and echo pins to PA3 and PA4 pins respectively on the STM32 Nucleo board.

* Open STM32CubeIDE and run the project

  ![Car Picture](https://i.postimg.cc/cCNcJRfc/Car.jpg)

# Iterations

## The First Milestone

- Integrating the Infrared sensors to try applying the lane detection
- Link For Demo: [Demo](https://drive.google.com/drive/folders/1-3KJ91FfxfCk9-20nycJq1BGQrZUv5BV)

## Final Milestone

- Integrating the ESP32 CAM to the STM32 Nucleo board to capture images and send them to the STM32 Nucleo board and process the image to detect and follow a lane.
- Using the ultrasonic sensor to detect objects infront of the car and stop it.
- Link For Demo: [Demo](https://drive.google.com/file/d/19p_erXYdElvhYQwuB0MS8_ObLfitgnJr/view?usp=sharing)

# How it Works

## Taking the picture

The ESP32 CAM takes a picture when it receives a signal from the STM32 Nucleo board. The ESP32 CAM then downsizes the image and sends it to the STM32 Nucleo board using UART2. Below is an example of the image taken by the ESP32 CAM.

![Image Taken by ESP32 CAM](https://i.postimg.cc/Kzfw2v8Q/kiroimage18.png)

## Processing the image

The STM32 Nucleo board receives the image from the ESP32 CAM and processes it to detect the lines using edge detection. An example of the image after edge detection is shown below.

![Image After Edge Detection](https://i.postimg.cc/3wBnyfQx/kiroimage17.png)

## How to move the car

A fisheye camera lens was used to capture a wider view of the road. This added a challenge to the lane detection algorithm as the two lane lines are not parrallel as seen in the image. Therefore the lane detection algorithm now simulates two lines that would have been the car tires' path and if these lines intersect the lane lines then the car should move in the opposite direction. For example, if the line from the left tire intersects a lane line the car should move to the right and vice versa. The image below shows the two lines simulated by the algorithm.

![Simulated Lines](https://i.postimg.cc/cHW7cRZ5/car.png)

## Next Steps & Future Work

- Try downsizing the image more to reduce the time needed to send the image.
- May want to use Radar instead of the ultrasonic sensor to detect objects infront of the car.
