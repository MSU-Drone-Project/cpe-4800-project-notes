# CPE 4800: Adviser's Capstone Project Notes

Adviser: Ivo Georgiev, PhD

Table of Contents
=================

* [CPE 4800: Adviser's Capstone Project Notes](#cpe-4800-advisers-capstone-project-notes)
  * [Project 1: Quadcopter Drone Flight Controller](#project-1-quadcopter-drone-flight-controller)
    * [Description](#description)
    * [Project Lead](#project-lead)
    * [Critical Path](#critical-path)
  * [Project 2: Quadcopter Drone Control with Motion Sensing](#project-2-quadcopter-drone-control-with-motion-sensing)
    * [Description](#description-1)
    * [Project Lead](#project-lead-1)
    * [Critical Path](#critical-path-1)

## Project 1: Quadcopter Drone Flight Controller
[[toc](#table-of-contents)]

### Description
[[toc](#table-of-contents)]

Making a flight controller for the Pluto X out of the Arduino nano and writing a BLE remote control app.

### Project Lead
[[toc](#table-of-contents)]

Arsene Ngollo

### Critical Path
[[toc](#table-of-contents)]

Project components and/or stages/milestones the success of the project depends on securing.

1. Understanding the drone.
   - (easy) watch the [videos](https://www.youtube.com/channel/UC4L7czrqbS7ebMf5dX5L1SQ)  
   - (medium) learn to fly the drone to understand what you are working on  
   - (medium) follow the [instructor's manual](https://www.dronaaviation.com/learn-instructors-manual/)  
   - (medium/hard) [program](https://create.dronaaviation.com/software) the drone (e.g. some of the tinkerer projects described by the vendor)  
   - (hard) read and understand the [firmware source code](https://github.com/DronaAviation/Magis)    
   - (medium/hard) fly the drone after tinkering with the code  
   - (medium/hard) study the [flight controller](https://create.dronaaviation.com/hardware/flight-controllers/primus-x) along with the firmware to understand what does what     
2. Understanding the [Arduino Babo 33 BLE Sense](https://www.arduino.cc/en/Guide/NANO33BLESense).
   - (easy/medium) familiarize yourself with the [NINA-B3 documentation](https://www.u-blox.com/sites/default/files/NINA-B3_DataSheet_%28UBX-17052099%29.pdf)  
   - (easy/medium) familiarize yourself with the [nRF52840 documentation](https://content.arduino.cc/assets/Nano_BLE_MCU-nRF52840_PS_v1.1.pdf)  
   - (easy/medium) familiarize yourself with the [sensor suite documentation](https://store.arduino.cc/usa/nano-33-ble-sense) (tab _Tech Specs_)  
   - (easy/medium) familiarize yourself with the [board documentation](https://store.arduino.cc/usa/nano-33-ble-sense) (tab _Documentation_)       
   - (medium) familiarize yourself with the connectivity of the board, specifically for your project  
3. Flight controller board.
   - (medium) design the flight controller board with all the components that you will need  
   - (medium/hard) design the mounting of the board on the Pluto X frame  
   - (medium) securing the Pluto X, control the motors with your FC board  
4. 3-axis (roll, pitch, yaw) PID loop.
   - (hard) fine-tuning will require an ingenuous "dry-fly" platform, where the drone is secure but still able to move (e.g. the drone suspended by 4 stretched rubber bands)  
   - (medium/hard) manual tuning might never converge, so you have to look for a config file that works for the Pluto X to use as a default, baseline, and starting point for fine tuning   
   - (medium) test the responsiveness of the drone with 3 axes (**critical** to know if the Arduino Nano 33 BLE Sense will be able to fly the drone)  
5. Control loop.
   - (medium) study how the commands for the Pluto X are actually implemented in firmware  
   - (hard) write your own control loop framework (you might need to limit the scope of the flight capabilities just to keep this possible)  
   - (hard) dry-fly test on your tuning platform  
6. Remote control with BLE.
   - (medium) establish communication over BLE between the Arduino and a mobile phone   
   - (medium/hard) design the BLE app (you might need to start from a skeleton app that you find out there; also, you should scope down from multi-platform to single-platform (whatever your phone is running, just to keep this possible) for the subset of commands you will want to program in the drone and whatever telemetry (real-time data from the drone) you will want to receive  
   - (hard) put the drone in the tuning platform and test the remote control from the app (app->(BLE)->Arduino->(pins)->ESCs+motors)  
7. Safety.
   - (medium) establish max distance for safe remote control  
   - (hard) hard-code safe autonomous ascent and descent   
8. Open-air test.  
   

## Project 2: Quadcopter Drone Control with Motion Sensing
[[toc](#table-of-contents)]

### Description
[[toc](#table-of-contents)]

Making a gesture recognizer out of the Arduino nano, programming the trajectories on the Pluto X and communicating over BLE between the wand remote control and the Pluto X.

### Project Lead
[[toc](#table-of-contents)]

David Ceniceros

### Critical Path
[[toc](#table-of-contents)]

Project components and/or stages/milestones the success of the project depends on securing.

1. Understanding the drone.
   - (easy) watch the [videos](https://www.youtube.com/channel/UC4L7czrqbS7ebMf5dX5L1SQ)  
   - (medium) learn to fly the drone to understand what you are working on  
   - (medium) follow the [instructor's manual](https://www.dronaaviation.com/learn-instructors-manual/)  
   - (medium/hard) [program](https://create.dronaaviation.com/software) the drone (e.g. some of the tinkerer projects described by the vendor)  
   - (hard) read and understand the [firmware source code](https://github.com/DronaAviation/Magis)    
   - (medium/hard) fly the drone after tinkering with the code  
   - (medium/hard) study the [flight controller](https://create.dronaaviation.com/hardware/flight-controllers/primus-x) along with the firmware to understand what 
2. Understanding the [Arduino Babo 33 BLE Sense](https://www.arduino.cc/en/Guide/NANO33BLESense).
   - (easy/medium) familiarize yourself with the [NINA-B3 documentation](https://www.u-blox.com/sites/default/files/NINA-B3_DataSheet_%28UBX-17052099%29.pdf)  
   - (easy/medium) familiarize yourself with the [nRF52840 documentation](https://content.arduino.cc/assets/Nano_BLE_MCU-nRF52840_PS_v1.1.pdf)  
   - (easy/medium) familiarize yourself with the [sensor suite documentation](https://store.arduino.cc/usa/nano-33-ble-sense) (tab _Tech Specs_)  
   - (easy/medium) familiarize yourself with the [board documentation](https://store.arduino.cc/usa/nano-33-ble-sense) (tab _Documentation_)       
   - (medium) familiarize yourself with the connectivity of the board, specifically for your project  
3. Understanding [supervised machine learning](https://en.wikipedia.org/wiki/Supervised_learning). 
   - (medium) understand that what you are doing currently with TinyML is **NOT** [transfer learning](https://machinelearningmastery.com/transfer-learning-for-deep-learning/), which is bleeding-edge ML and still largely unsolved  
   - (easy/medium) read the first few chapters of Andrew Trask's _Grokking Deep Learning_  
   - (medium) with this knowledge, take apart the pipline you used from the example, and explain to yourself every step   
4. Understanding _motion-sensing for control_ in terms of reference frames.
   - (easy/medium) **TODO**  
5. Gathering gesture training data.  **TODO**  
6. Training the model.  **TODO**  
7. Recognizing the I2C BLE transceiver.  **TODO**  
8. Communication over BLE between Arduino and BLE transciever.  **TODO**  
9. Programming the trajectories.  **TODO**  
