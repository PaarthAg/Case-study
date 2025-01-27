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

1.3.Tyres: 

To traverse in the M-sand area the rover used wheels of the following properties:-

-Metal Rim

-Hard rubber tyres with structured pattern of hard rectangular bumps that help the rover to generate the friction needed to travers the M sand. THe rubber plus the bump helps the rover to easily traverse the 15cm cube with the bump treading over the block and rubber providing the required friction to generate the upwards force that helps the rover climb.

-![image](https://github.com/user-attachments/assets/4f884ceb-c308-40f8-b8d7-292564f4866b)

-The slow speed and ability to climb the 15 degrees slope shows us the power of its motor, meaning that the motors used priortize on torque and not angular speed.

-The radius of the wheel seems to be greater than the height of the block out of the M-sand, that is 15cm. This enables th wheels to climb over the block much more easily and require much less force to generate enough friction to climb over the block. This also eases the wheels movement throught the 20cm diameter crater and makes the overall ride of the rover very smooth.

1.4.Camera System:

-The team relies on openCV technology to train the robot of the different obstacles using machine learning and helps the rover to detect all the different obstacles and the different sample targets and drop points.

-![image](https://github.com/user-attachments/assets/b876baa9-2557-463b-83c5-a2403ed4e536)

-![image](https://github.com/user-attachments/assets/38b4c190-d494-436a-b498-34a1560c4219)

-![image](https://github.com/user-attachments/assets/a4685936-c58b-4bb8-b474-6fba291ec0c7)

-![image](https://github.com/user-attachments/assets/0fa88e7b-5ce1-4015-8cef-e7c570f7896a)

-It is seen that the robot uses only one onboard camera which helps it detect the blocks, sample target and drop point.

-The detection of the different objects is a result of training an AI model using machine learning to be able to detect the objects and the object's annotations helps the rover to make decisions about the detected objects.

1.5.Electronics used:

-All the calculations, running of program, openCV detection and the sending of all the data collected (obstacles encountered and camera feed) is happening on the Jetson Orin Nano computer.

-Jetson Orin Nano is a developer board designed by Nvidia, and the board is designed to be able to process high load tasks such as running generative AI which helps the robot in this function to use AI and openCV to detect the elements in the challenge. The board is good enough to run all the algorithms that would ever be needed to complete this challenge making it the best option for this challenge. The cost will also not be a major issue as the board costs from 20,000 INR (Super model) to 77,000 (Normal model) and can be reused for the further projects that might be done by the team.

1.6.Manupilator:

-The manupilator used by team obseract is of a screw type system in which one jaw of the manupilator stays still, there is an axle passed through the jaws which has threads and works like a screw to help the other jaw move by rotating the screw type axle. This jaw is good as the rotation of motor can be very precise, hence making the manupilator go easy on the samly tube and not exert too much pressure on the tube as good care of tube also carries some points.

-The jaws are distanced enough to pick up the sample tube in any orientation and there is only one degree of movement of the arm as approaching towards the sample object is done by the drive of the rover itself, hence the only degree of movement left is the one which helps the arm go up and down like the shoulders of a human arm.

-![image](https://github.com/user-attachments/assets/7d0836e4-80c1-4b9d-96c0-20086d67d37f)

-
