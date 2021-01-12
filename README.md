# CPE 4800: Capstone Project Notes

Adviser: Ivo Georgiev, PhD

Table of Contents
=================

* [CPE 4800: Adviser's Capstone Project Notes](#cpe-4800-advisers-capstone-project-notes)
  * [Project 1: Quadcopter Drone Flight Controller](#project-1-quadcopter-drone-flight-controller)
    * [Description](#description)
    * [Project Lead](#project-lead)
    * [Critical Path](#critical-path)
    * [Scope Progression](#scope-progression)
  * [Project 2: Quadcopter Drone Control with Motion Sensing](#project-2-quadcopter-drone-control-with-motion-sensing)
    * [Description](#description-1)
    * [Project Lead](#project-lead-1)
    * [Critical Path](#critical-path-1)
    * [Scope Progression](#scope-progression-1)

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

**TODO** Requires more detail for Points 4 and 5

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
4. **3-axis (roll, pitch, yaw) PID loop.**
   - (hard) fine-tuning will require an ingenuous "dry-fly" platform, where the drone is secure but still able to move (e.g. the drone suspended by 4 stretched rubber bands)  
   - (medium/hard) manual tuning might never converge, so you have to look for a config file that works for the Pluto X to use as a default, baseline, and starting point for fine tuning   
   - (medium) test the responsiveness of the drone with 3 axes (**critical** to know if the Arduino Nano 33 BLE Sense will be able to fly the drone)  
5. **Control loop.**
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
   
### Scope Progression

A sequence of stable milestones of partial end-goal completion which work in their own right and can serve as flexible surrogate end-goals for dynamic scope control.

**TODO**  

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
3. **Understanding [supervised machine learning](https://en.wikipedia.org/wiki/Supervised_learning).** 
   - (medium) understand that what you are doing currently with TinyML is **NOT** [transfer learning](https://machinelearningmastery.com/transfer-learning-for-deep-learning/), which is bleeding-edge ML and still largely unsolved  
   - (easy/medium) read the first few chapters of Andrew Trask's _Grokking Deep Learning_  
   - (medium) with this knowledge, take apart the pipline you used from the example, and explain to yourself every step   
4. **Understanding _motion-sensing for control_ in terms of reference frames.**
   - (medium) the drone has its own _reference frame_ (exactly where it falls depends on their design; actually, the drone has 2-3 different reference systems and they are corrected for in the firmware: IMU, center of mass, center of thrust), relative to which it will perform any trajectory it's (programmed and) commanded to   
   - (medium) the Arduino has its own 2 systems: IMU and center of mass; you might or might not need to correct for it   
   - (medium) a _gesture_ is performed **relative** to the egocentric center of mass of a human (Actually, that's a gross simplification. For example, you can perform a hand guesture relative to your wrist and it will be recognized regardless of what the rest of your body is doing. _The human mind absolutely does not do [inverse kinematics](https://en.wikipedia.org/wiki/Inverse_kinematics) to recognize gestures._ The simplification will work for this project. However, it might need to be corrected for for the next point.)  
   - (hard/very hard) for the training of the Arduino to recognize gestures, the IMU data may or may not need to be translated to the human frame:
     - if it is not, the data might be too _noisy_ to learn a good _gesture classifier_: this means that, since the data from the IMU is naturally relative to its own reference frame, the datapoint sequence for the gesture motion **does not** describe a gesture relative to the IMU; as a result, the learning algorithm and the model structure might not be able to _generalize_ well and the classifier will be very glitchy      
     - if it is to be translated, the human reference frame will need to be fixed in space-time (this can either be approximated by aggregating [anthropometric data](https://www.google.com/search?q=anthropometric+dataset) or it has to be a physical device (e.g. another Arduino Nano 33 BLE Sense) to close the loop for time-of-flight (TOF) measurements for relative position) (if you wonder why we need this, read on [oculus controller headset communication](https://www.google.com/search?q=oculus+controller+headset+communication) - the headset is the reference and the the two controllers are tracked relative to it and to each other)  
   - (medium/hard) there might be a _simpler_ workaround the previous item, but for this requires understanding of the following points:
     - machine learning is based on _features_, roughly defined as patterns of coocurrence of certain data that are repeatable and recognizable; in the beginning, these features had to be programmed by hand; with _deep learning, the model structure allows the model to extract the features automatically - this resulted in an explosion of novel solutions; for example, a feature might be a characteristic bump in the graph of a function  
     - the reason _"punch"_ and _"flex"_ work is subtle, and it has to do with features; they are very abrupt and fast motions, and generate very good accelerometer features; if the "gesture" motion is slower and smoother, the features will not exist; for example, performing a circular motion to command the drone to repeat it, will not generate data that will be recognizable as a "circle" without translation to the human reference frame   
     - one solution _might be_ to perform very fast tight circles and figure-eights (I advised to do this several times during the Fall semester)    
5. Gathering gesture training data.   
   - (easy) define the "gesture motions"     
   - (medium) come up with a setup and procedure to capture the motion data and pair the data sequence with a gesture _label_ (e.g. "Circle", "Figure-8", etc.)  
   - (easy) have several people perform each gesture 100s of times and assemble a _training dataset_  
   - (medium/hard) preprocess the data in accordance with item (4) above  
6. Training the model.  
   - (easy) make a randomized split of the dataset into [_training_, _validation_, and _test_ sets](https://towardsdatascience.com/train-validation-and-test-sets-72cb40cba9e7) with the ratio 8:1:1  
   - (medium) customize the TinyML pipeline for your data  
   - (easy/medium) train the model, using the dataset splits    
   - (medium/hard) come up with a mothod for live reading the gesture classification; this will be used for testing in the physical world  
7. Recognizing the I2C [BLE transceiver](https://www.dfrobot.com/product-1259.html) (aka Beetle) by the FC.  
   - (easy) create the I2C connector from the breakout to the Beetle (you do not want to solder headers; the best would be if you a swisted copper wires and solder the copper directly to the SCL and SDA contacts)  
   - (medium) add the I2C device to the firmware, set up a passive repeater test to make sure the FC and the Beetle can communicate, reload the firmware, and test    
8. Communication over BLE between Arduino Nano and BLE transciever.  
   - (medium/hard) write basic code for FC firmware and Ardiuno Nano to communicate over BLE (this should just be a handshake); a complete readout of the protocol exchange will be very helpful  
   - (medium) add new commands to the FC firmware for the trajectories you will want to perform  
   - (medium) add automatic ascend and land commands to the Arduino nano  
9. **Programming the drone trajectories.**  
   - (hard) program the trajectories corresponding to the gestures that will be made (this is in the firmware)    
   - (hard) come up with a way to add the commands to the controller app, to test the trajectories in the air (without a wand)    
10. Beetle mounting.  
    - (easy/medium) design the attachment of the BLE transciever and do a test flight    
11. Wand design and operation. 
    - (easy/medium) design the buttons and program, interrupt handlers for them, and test their operation and the responsiveness of the Arduino  
    - (easy) design and build the battery case and the power connector to the Arduino  
    - (medium) design the case with three buttons
12. Safety.  
13. Open-air test.  

### Scope Progression

A sequence of stable milestones of partial end-goal completion which work in their own right and can serve as flexible surrogate end-goals for dynamic scope control.

Milestone | Project component | Demo
--- | --- | ---
1 | 8 | Hook up the Beetle BLE transciever to the I2C bus of the Smraza Uno R3 board and establish a two-way BLE link with the Arduino Nano 33 BLE Sense.  
2 | 7 | Hook up the Beetle BLE transciever to the I2C but of the Primus X flight controller and establish a two-way BLE link with the Arduino Nano 33 BLE Sense.
3 | 9 | Program the Pluto X to perform two trajectories (circle and figure-8) autonomously from the stable hovering position following the completion of the "Take off" command from the remote (phone). Add the commands "Circle" and "Figure-8" to the firmware, just like the "Take off" and "Land". _How to you add a command to the remote (phone) control?_
4 | 10 | Mount the Beetle onto the Pluto X.
5 | 8 | Demonstrate that the commands "Circle" and "Figure-8" can be sent from the Arduino Nano 33 BLE Sense over BLE to the Beetle and over I2C from the Beetle to the Primus X, and that the Primus X recognize them as valid commands.
6 | | Using the controller app, get the Pluto X to hover. Send the trajectory commands "Circle" and "Figure-8" from the Arduino Nano 33 BLE Sense and get the Pluto X to execute them, one at a time. Using the controller app, get the Pluto X to land.
TBD | 3-6 | After successful completion of Milestone 6.

