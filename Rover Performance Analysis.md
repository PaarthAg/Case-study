Introduction: In this document we are going to analyse the robots of different team that participated in the ISRO robotics challenge 2024. There were only 20 teams that qualified for the field round.

Contents:

1.**Team Obseract-Jadavpur University**:-


1.1.Size and weight: size: 87cmx70cmx77cm, weight: 39kg


1.2.Suspension system:

-The team obseract has used a rocker bogie suspension system which is expected to be a common trend throughout this competition due to its simplicity and the ability to traverse through the 15cm cube (it is known to traverse over the 20cm obstacle easily) and the 20cm diameter crater very easily.

-The rocker bogie system has a simple concept in which the last 2 wheels support the rover while the first wheel climbs the obstacle, next when the first wheel has cleared the obstacles then the second wheel is able to lift with the help of the bogie part of the assembly. till then the 3rd and the first wheel provide the required support and at the end the bogie helps the 3rd wheel rise as the 2nd and 1st wheel hold on the rover.

-This system is not that complex, easily folds hence easy to carry.

-This system in real life applications is attached with an acutator and deployment system that increases its length by 17 cm to be able to climb steeper angles as 45 degrees was found to be the max limit in the initial designs.

-![image](https://github.com/user-attachments/assets/c717fc17-4659-427b-96d2-8a4d987a4843)

Here MER is Mars exploration rover.

-The use of Rocker bogie suspension makes it obvious that diffrential driving technique is used to turn to robot for all the cases and the slow speed of the rover helps the rover to make very minute turns, which further helps us eliminate the use of another degree of movement for the manupilator and the drive itself aids the manupilator in pickup of the sample accurately.


1.3.Drive: 

To traverse in the M-sand area the rover used wheels of the following properties:-

-Hard rubber or 3D print plastic tyres with structured pattern of hard rectangular bumps that help the rover to generate the friction needed to travers the M sand. THe rubber plus the bump helps the rover to easily traverse the 15cm cube with the bump treading over the block and rubber providing the required friction to generate the upwards force that helps the rover climb.

-![image](https://github.com/user-attachments/assets/46dde39b-7a50-4672-b249-747e3d6312a6)

-The slow speed and ability to climb the 15 degrees slope shows us the power of its motor, meaning that the motors used priortize on torque and not angular speed.


1.4.Camera System:

-The team relies on openCV technology to train the robot of the different obstacles using machine learning and helps the rover to detect all the different obstacles and the different sample targets and drop points.

-![image](https://github.com/user-attachments/assets/b876baa9-2557-463b-83c5-a2403ed4e536)

-![image](https://github.com/user-attachments/assets/38b4c190-d494-436a-b498-34a1560c4219)

-![image](https://github.com/user-attachments/assets/a4685936-c58b-4bb8-b474-6fba291ec0c7)

-![image](https://github.com/user-attachments/assets/0fa88e7b-5ce1-4015-8cef-e7c570f7896a)

-It is seen that the robot uses only one onboard camera which helps it detect the blocks, sample target and drop point.

-The detection of the different objects is a result of training an AI model using machine learning to be able to detect the objects and the object's annotations helps the rover to make decisions about the detected objects.

-The team also uses a depth camera, which can measure the distance between itself and the objects using time taken for infrared signals to bounce back to the camera. The camera hence is able to make a 3D image of whatever it is seeing and makes this the perfect camera for such a project. This camera also reduces the need of using different techniques in openCV to find the distances between 2 objects by using 1 as refrence.

-![image](https://github.com/user-attachments/assets/b466e60e-939b-46ff-9a96-b24426904540)


1.5.Electronics used:

-All the calculations, running of program, openCV detection and the sending of all the data collected (obstacles encountered and camera feed) is happening on the Jetson Orin Nano computer.

-Jetson Orin Nano is a developer board designed by Nvidia, and the board is designed to be able to process high load tasks such as running generative AI which helps the robot in this function to use AI and openCV to detect the elements in the challenge. The board is good enough to run all the algorithms that would ever be needed to complete this challenge making it the best option for this challenge. The cost will also not be a major issue as the board costs from 20,000 INR (Super model) to 77,000 INR (Normal model) and can be reused for the further projects that might be done by the team. The one big flaw in the nano developer module is that its software and user interface is very bad and has been a problem for many developers.

-For communication the team has used Ubiquiti LiteBeam M5 Antenna which operates in 5 GHz band and 23dBi gain which means that the antenna works really well for long distances and works with radio waves which makes this antenna very good for this project. The antenna is compact too hence does not trouble the design of the rover. The antenna uses a SISO (single input single output) system which makes it cheaper and simpler than a MIMO system which would had used multiple antennas and would have been costly (an overkill for such a project).

-The team has also used gyro sensors/ angular velocity sensors to be able to know the yaw, pitch and roll of the robot, which must help rover know that how much power is needed by the motors and what elevation are they in, which further saves power and reduces the load on the battery.

-For Gyroscopic and acceleration sensing the team has used an IMU sensor, which is multitasks to know the orientation and the velocity of the rover. IMU consists of 3 accelerometrs, 3 gyroscopes and 3 magnetometers. The program integrates the acceleration data once with respect to time to find the data of velocity. They used the BNO-055 IMU.

-Even though the velocity data of accelerometer is ot that accurate, the slow speed of robot and the help of suspension in reducing the effect of external forces the error is not that significant in such a case.

-![image](https://github.com/user-attachments/assets/e2147f7c-cf11-40e8-86e1-65eb2ad8b5f5)

-The team uses also uses a STM32F407VET6 DEV MODULE to run the rover. The module is very good very good for such applications, details about STM32F407VET6 are:-

1.Uses ARM Cortex M4 core with a floating point unit. Here Arm cortex M4 is a 32 bit micro processor and floating point unit is a hardware device that does mathematical operations on the floating points, the FPU is mostly used for digital signal analysis and control systems.

2.The ARM Cortex M4 microprossecor uses DSP (digital signal processing) and hence it can be used to process all the data from the sensors and process them very efficiently. This includes digital to analog and anlog to digital conversion. This process uses the help of FPU.

3.High clock speed (upto 168M MHz)

4.Multiple communication interfaces, ie. USB, SPI, I2C and USART. Out of these options chances are that they used USART as USART is used for serial communication for longer distances (radio waves in this case), where as the SPI and I2C are used for communication between 2 different components of a circuit, such as the microprocessor and the sensors in the same circuit. Also the USART comes with error detection systems and can support asynchronous communication, so there is no need for a clock to be set and helps better for longer distances. The USART system needs wires, just that the data is tranmitted using antennas, transmitters and recievers.

-The Jetson Orin Nano and the STM32F407VET6 can be used together in the same robot as the Nano will be used for processing images (openCV applications) and run all the algorithms and at the same time the dev module will be used to manage the motors and all the other sensors that do not require high ammounts of processing. The 2 developer boards will co-exist in the rover. The team here used the STM32F407VET6 DEV MODULE  to control the robotic arm by taking the data from the camera processed by the jetson orin nano, and another board (not specified, maybe STM32F407VET6 or the Nano) is used for the control of the wheel drive.


1.6.Manupilator:

-The manupilator used by team obseract is of a screw type system in which one jaw of the manupilator stays still, there is an axle passed through the jaws which has threads and works like a screw to help the other jaw move by rotating the screw type axle. This jaw is good as the rotation of motor can be very precise, hence making the manupilator go easy on the sample tube and not excert too much pressure on the tube as good care of tube also carries some points.

-The jaws are distanced enough to pick up the sample tube in any orientation and there are 3 degree of movement of the arm: first approaches towards the sample object like the human elbow , the second helps the arm go up and down like the shoulders of a human arm and the third one is which twists the claw 360 degrees like the human wrist, this one helps to pick up the sample tube in its specified orientation.

-![image](https://github.com/user-attachments/assets/c4a848f8-10cb-4b78-bc65-02c9a9cfccca)


1.7.Algorithms: No information to be found obout their game plan and their algorithms



2.**Team Samarth - Sharda University**:-

2.1. Size and weight: size: 98cm x 57cm x 73cm, weight: Unspecified.

2.2. Suspension system:-

-This team too uses rocker bogie mechanism due to its simpicity and ability to do the required tasks very easily. They have used PVC pipes with a coating of acrylic paint for the suspension, this is due to its ability to support very heavy loads and its light weight.

-The team has also used 2 cross suspension, ie. 2 hydraulic suspensions connecting bogie with the main chasis of the rover. This suspension ensures smooth ascend and descend of the rover at each of the obstacles and helps the overall smoothness of the ride of the rover.

-This team too uses diffrential drive mechanism for turning.

2.3. Drive:-

-The design of the tyres used by team samarth is very unique as the tyre is not one continous cylinder, and the cleats of the tyres are in different directions too.

-![image](https://github.com/user-attachments/assets/0970100c-5f5d-4607-840c-507c36ee6d49)

-The wheels are 3D printed with the PLA material which are sturdy enough to support the whole rover.

-The cleats are similar to the ones that were used by team obseract but the design of wheel is way different.

-The discrete wheel offers better traction in the M-sand arena, and also makes it very easy to climb over the 15 cm blocks.

-This unique design also allows the rover to have smaller wheels as the climbing part eases out with the help of the design.

-The motors used in the drive are able to produce 10 RPM and 600 N-m torque, showing us the importance of the low angular velocity high torque motors in this challenge.


2.4.Camera systems:-

-This team too uses openCV to detect the objects.

-The team has used a normal webcam which tranmits feed to the computer, the output of this camera is used for openCV.

-The team uses anoter camera mounted at the very top of the rover, this is a FPV camera which is used in drones and this camera transfers analog feed to the ground station computer.

2.5. Electronics used:-

-The system uses 5.8 GHz frrquency to communicate witht he control base and show the telemetry feed.

-The transmitter reciever system for the rover is: transmiter:TS832 FPV transmiter, Reciever: RC832. This transmiter reciever pair is mostly used in FPV drones and show a very low latency feed.

-For data transmission the team uses NRF24L01 PA LNA trans reciever module which operates on 2.4 GHz frequency and is used by the team to transmit data such as the data of the distance which is calculated live by the ground station computer.

-The team mentions using a self designed motor driver board which is responsible for the precise movement of the motors during the mission.

-Raspberry pi 4 (8 GB ram) computer is used by the team to process the information, this development board has the following properties:-

1.64 bit processor.

2.Quad core processor: This means that the processor is divided into 4 cores, out of which each core performs multiple tasks simeltaneously, which makes this a really strong processor for such a project.

3.Is compatible with 2.4 GHz and 5 GHz frequency for communication, making it better for the already chosen transmitter reciever pair.

-The raspbery pi has a very powerful processing unit and is capable enough to run the openCV commands on the rover itself and then command the motors to take the further actions.

-The rover does not limit itself to cameras, but uses LIDAR and ultrasonic sensors too.

-The use of ultrasonic sensors is a bit illogical here as if the rover is being made to traverse on extraterrestrial surfaces such as the moon, hence the ultrasonic sensors rould not be applicable there making it only functional for the earthly environments, a better alternative would have been the use of IR sensors which do the same work, but use infrared light rays to measure distance unlike the sound used by the ultrasonic sensors.

-Lidar is a great techology to be used on this rover, where the surroundings will be clear (no rain or dust) and LIDAR has pinpoint accuracy, helping the rover map its surroundings and not bash into any obstacle.

-The team has used the mini LIDAR (Time of flight) sensor as it is able to easily fit in the rover and calculates the distances of objects in front only.

2.6. Manupilator:-

-The manupilator has 3 degrees of freedom:-
1.Helps the manupilator reach forward.(elbow)
2.Goes up and down.(shoulder)
3.goes sideways.(shoulder)

-The manupilator uses 5 25kg torque motors for high accuracy.

-The teams are noticed to be using inverse kinematics to find the exact location of their claw and be able to pick up the sample tube. Even team obseract used this technology.

-The manupilator jaw is a simply mechanism and is very gentle as the tube used by the team to demonstrate was made of paper and the manupilator did not crush it.

-The robot is able to self analyse the amounts in needs to move to be able to grip the sample tube and drop it.


2.7.Algorithms:-

-The Robot uses the webcam to detect the sample tube and then uses inverse kinematic calculations to be able to tell that how much it needs to move in what direction to be able to securely hold the sample tube. 

-The robot uses openCV to detect the sample target and the the sample container and uses lidar + openCV to measure the distance of the rover from the object.

-Next the rover starts to rotate clockwise until the blue sample is in linear alignment to the rover and then starts to surge towards the container.

-If in between the rover senses that any non traversable obstacles may colide with any of the parts of the rover, the robot mooves away to a safe distance from the obstacle and still keeps moving in the direction of the container, in this process te rver still detects te traversable obstacles.

-Finally after reaching to the final point the rover again uses inverse kinematic calculations to plan a path of the manupilator to safely drop the sample in the drop point. After the drop, the rover analyses its surroundings and moves out of the final point safely and parks itself.


3.**Team shunya - IIITD Kancheepuram**:-

3.1.Size:-

-Weight: 48.8 Kg

-Size: 97cm x 71cm x 60cm 

3.2.Suspension system:-

-This team uses a unique triple bogie system for this robot.

-In this system the front 4 tyres are connected parallel to each other by bogie mechanism on each side and the the 2 tyres behind are connected to each other by another bogie mechanism.

-The rocker bogie system is not better than the rocker bogie system for the applications of this project as the triple bogie system is phenomenal for load bearing as it has more support and is more stable, but that is not the task in this challenge, the use of the triple bogie system is more complex, uses more materials and is not better than rocker bogie system for traversing in a rough terrain. The challenge does not show much emphasis on the rover's ability to traverse through a very rough terrain, for which rocker bogie would be would had been the best option if aiming for simplicity, but in this competition triple bogie suspension wouldd work just fine, but may require the use of more materials.

-On the other hand the triple bogie system undeniable makes it much more simples to fit the steering system on the the rover, hence making it a better choice for the use of the steering system rather than the diffrential drive mechanism.

-The suspension system is made using sheet metal as the metal is strong enough for our applications and the metal is light, helping the rover be under 50 Kgs weight limit.

-![image](https://github.com/user-attachments/assets/a5b44828-7a9d-4668-8be4-cacff5fbfd8e)


3.3.Drive:-

-The wheel mount and the wheel are made using sheet metal and some plastic parts. Sheet metal is easy to bend, making it easy to morph into the desired shape and keep the system light while being sturdy.

-![image](https://github.com/user-attachments/assets/960185d5-847f-4ab2-8f70-da2e236885a1)

-As we can see the design of the wheels is very unique as the wheels use a specific cleat shapes that is able to push the sand backwards and help the rover in moving forward with great traction.

-The curved design of the cleats is specifically for the ease of turning of the wheels without any vibrations.

-2 RMCS motors are used for 4 each wheels and 1 each for 2 (middle wheels). One RMCS is used for turning and the other is used to rotate the wheel.

-The use of RMCS motors is a good decision due to its high torque output and its inbuilt encoders helping the motor to make precise movements.

-![image](https://github.com/user-attachments/assets/3a75afac-70ec-47c5-bade-bd48700823eb)

-The rover uses encoders as a feedback mechanism for the steering part of this system.

-This team is unique in the terns of using a steering mechanism rather than a diffrential drive mechanism. This mechanism has the following advantages and disadvantages:-

1.Advantages:-

i)Easy on-point turning.

ii)More accurate turning.

iii)More versatile movement.

iv)The rover saves time on going back and then turning back to the direction it wants to go, here the rover will turn into any direction it wants t go to instantly and then thart moving.

2.Disadvantages:-

i)Cost of motors add up.

ii)The gear mechanism occupies more space.

iii)The wide design of the wheels forces the rover to stop, turn the wheels and then move, hence making it slower.

-As we can see there are many advantages and disadvantages of this system. But the team prioritizes on accuracy of their movement with efficiency over saving volume and money, hence they use the steering mechanism.

-The steering motors are given +60 to -60 degrees freedom of movement to each of the turnable tyres.

-PID control system is needed for precise movement control with taking feedback from the encoders.

-The drive system is integrated with the motor controlling software witht the help of ROS serial. ROS serial is a protocol that enables the communication between a computer and a microcontroller (like arduino). This makes the microcontroller a ROS node and then the microcontroller is connected to the ROS computer and then transmission of data can happen easily between the computer and the microcontroller, so if there is some complex processing that the microcontroller is not able to do by itself, the ROS helps the microcontroller by connecting it to a computer which can perfom tasks like openCV and then give direct commands to the microcontroller. ROS is advantageous in the sense that it makes a simple ROS system which in a way connects the sensors and the actuators directly to the computer.

-The steering mechanism uses gears to reduce the vibrations that may occur while turning the wheels by other mechanisms. This is necessary because the rover uses camera and depth cameras to map its surroundings by making laser scans, but if there are too many vibrations, then there would be too much error in the mapping, which can make the whole mission to go into shambles.


3.4.Camera Systems:-

-The rover uses the ZED 2i stereo camera which offers the following:-

1.RGB data, useful for colour detection of the sample target ad the drop point.

2.Depth perception, the camera uses infrared time of flight sensors to measure the distance of different objects from the camera.

3.The camera also provides point cloud data, that means that the camera maps the areas it can see and make a 3D map of each of the detected elements, making the algorithms written for the rover to avoid obstacles and movement towards the targets much more simpler.

-The manupilator uses another different camera which uses openCV to detect the drop point and the sample target, and helps the manupilator to pick up the sample target precisely.

-The rover uses depth image to laser scan package as the depths percieved are converted into laser scans, which helps massively in the mapping done by the camera system.

-The team prefers to use SLAM mapping package which automatically takes data from ZED 2i stereo camera and maps it in a plane in real time, hence enabling it to map the surroundings as the rover keeps on moving. The team uses G-Mapping which uses the laser scan data to create the map. G-mapping is a part of the SLAM algorithm andd helps a lot in this project by seamless mapping of the arena.

-![image](https://github.com/user-attachments/assets/b47892cb-83e3-40d3-ac76-ab3d53d51bd5)

-This mapping system helps the rover to navigate much more easily through partially mapped or completely unkown areas. The technology drastically reduces the stress for the algorithms part.

-The openCV detection process is done by YOLO 8. YOLO is an algorithm which has a library of objects that it can detect by the camera feed, or you can use machine learning to train YOLO the objects that you desire, then the YOLO algorithm can detect the objects that you have trained it to detect. To enable detection, we use graphic view softwares to annotate the images with the objects and then that annotation's image data is stored in a class (class name is chosen by us) by the annotation program and then after further processing we have the YOLO ready to detect our desired objects. This is called transfered learning which this team has used in this rover.


3.5.Electronics used:- 

-The motors and sensors usedd are the same as the ones specified in this whole report, ie. RMCS motors which have inbuilt encoder, stepper motor, force sensor, ZED 2i stereo camera which has depth camera in it.

-Potentially an IMU was being usedd to find the orientation of the rover hence helping the the stability of the mapping done by the robot.

-There was no information specified on the Circuit boards, developer boards used. It was specified that they made their own PCB for the processing of the data, but no further ddetails were given.
3.6. Manupilator:-

-The robot is claimed to have 5 degrees of freedom out of which the usual elbow and shoulder joints are obvious and the other 2 degrees can be of the wrist joints.

-Each joint is using RMCS high torque motors and encoders for very precise movements.

-The claw is powered by rotating gears that turn a worm gear and then on them slide our grippers, which enable very gentle pickup of the sample tube.

-The manupilator uses materials like the Aluminium 6061 due to it being light weight yet sturdy. They also use PETG for 3D printing beacuse of its strength and light weight.

-The team uses servo motors in the claws' mechanism because of servo motor's accurate and controlled rotation.

-The manupilator is assisted by a camera that instructs the manupilator in real time to be able to precisely pick up and drop the target.

-The team mentions using force and stress sensors in the manupilator too, this maybe done to detect when the gripper has gripped the sample target firm enough and help the rover not over exert on the sample target.

-The team also uses pulley mechanisms in the arm links to have much more accurate and precise movements.

-The pulley mechanism helps the robot to concentrate the weight of the motors at the centre of the base, making the manupilator's movements much more predictable and stable.

-![image](https://github.com/user-attachments/assets/cb4adfdb-ba5d-47dd-a770-00afd3a35660)

-Other than the RMCS motor and the servo motor at the gripper the rover has a stepper motor has been used in the assembly, this motor is highly precise and gives the count of how much it has moved.

-The RMCS motors have encoders in them, so they give the value of encoders as an input to the computer too.

-The Team uses PID for error correction and much more precise movements, the PID uses position as feedback loop, which means that the position of manupilator is constantly update with the use of stepper count, encoder's information and the data sent by the camera, and the motors are tasked to move just enough that the manupilator aligns with the desired position and then keeps on repositioning until the manupilator is precisely at the required position. The PID does this with the analysis of 3 factors: The current error (proportional), the accumulated past errors (integral) and the rate of change of error (derivative).

-The whole system is powered by a 12V battery.

-The manupilator also applies limit switches. Limit switches are such switches which detect that a mechanical part has reached a certain point using any actuators and notifies the same to the system. These switches are mostly used for safety purposes in many machines (safety of the machine).


3.7.Algorithms:

-The rover first starts in the command/pre-programmed mode which is good enough to help the rover to reach to the way-point. But during this process the rover keeps on mapping the arena.

-After reaching to the way point, the manupilator camera start to look for the sample target using openCV, then the algorithm uses the position of sample tube to be the target position, the encoders of RMCS high torque motors give the current position of the manupilator, then the algorithm uses this as the feedback for the PID and keeps on changing the position of the manupilator constantly with the help of the algorithm and picks up the sample tube with absolute accuracy.

-Then the rover uses the pre mapped information of the arena and its current positions its dimensions to trace the best path to the drop point, it is able to detect each of the traversable obstacles that is was not able to see before but just rams over them. Then the rover uses its steering, which is controlled by the drive controlling software to find which way does it need to turn for how much angle and time. The angles are decided by running kinematic calculations to trace the most optimal path.

-After reaching to the final point, the rover's main camera and the manupilators camera coordinate to find the droping container and the sample target is dropped in the same manner that it was picked up.

-THen the rover will just back out of the final point using the mappe surrouning's data.
