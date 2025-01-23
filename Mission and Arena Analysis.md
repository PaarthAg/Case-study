For the Qualifiers round:
Arena:
The arena for ISRO robotics challenge URSC-2024 is:-
1.	Size of arena: 5m x 10m
2.	Filling material of arena: M-sand
3.  Sloped terrain: A sloped terrain with inclination of 15⁰ and inclined length of 2 m filled with M-sand and distributed with obstacles and craters.
4.  Obstacles: Cubes of sides 150 and 300 mm. The obstacles will be made from wood and planted firmly in the Arena. The rover traversal over them will not disturb their position.
5.  Craters: Craters are created by scooping out sand from the arena. These craters will be
    approximately hemispheres with diameter 200 and 400 mm.
6.  Boundaries of the arena will be marked distinctly.
7.  The starting point (SP) is a 1200mm x 1200mm square block at the corner.
8.  The way point is the point from where the rover will identify and pick up the test tube, it will be 1100mm x 1100mm.
9.  The target point (FP) is located in a 1500mm diameter circle, this is where the sample container will be located, in which we need to put the sample test tube.
10. The sample test tube is of red colour and has the following dimensions: OD=80mm, ID=70mm, Length=125mm, Mass=200gm (+-10gm error).
11. The Sample container is of blue colour with the following Dimensions: ID=150mm, Length=150mm.
12. ![image](https://github.com/user-attachments/assets/7889b241-b0fa-4ada-bb2a-12df0d32e5b8)


Rover and Manupilator (Arm) requirments:
1. The robot should not be connected to any GPS or such external navigation systems to simulate the extraterrestrial conditions.
2. The Robot may use Radio Frequency to communicate in order to control the robot. The range of the radio frequency must be 15m-20m minimum, 25m is the maximum that the rover will go away from the controller.
3. A legal radio frequency must be used to control the robot.
4. The battery pack must survive the whole of the mission time without any replacement.
5. All rovers must be equiped with a big and visible kill switch which must draw out all power from the batteries if needed.
6. the speed rang of the rover is fro 1cm/s to 50cm/s.
7. THe rover must be operation in temperatures ranging from 20 degree celsius to 40 degree celsius.
8. Use of readymade robotic kits is not allowed
9. Pwer efficiency will be accounted in the evaluation.
10. ![image](https://github.com/user-attachments/assets/9d3d0c77-0327-48de-af5a-a9c1e2fc0e57)


Task:
1. Segment 1: Commanded Waypoint Navigation
    Rover should move from starting position to waypoint ‘WP’ in a commanded manner and must navigate obstacles ‘2’, ‘12’ and ‘4’. The path planning can be done offline and rover can be commanded with exact path for this        segment. Failure to traverse any obstacle mentioned earlier will attract penalty points.
    Objectives of this segment include demonstration of rover capability to
    1. navigate obstacles
    2. follow commanded path

2.  Segment 2: Autonomous Sample Pick Up
    After arriving at the waypoint, rover must autonomously
    1. Identify the sample
    2. Approach the sample
    3. Pick the sample
    All these tasks must be accomplished autonomously without intervention of the team members (physical or otherwise). In case of contingency or failure of autonomous mode, commanded mode can be exercised and this will         attract penalty points.

3. Segment 3: Autonomous Navigation
    Picked-up sample must be transported to the sample drop position while navigating the obstacles autonomously. All obstacles (cubes and craters) must be identified by the onboard sensors and appropriately avoided by          rover mobility system to plan optimal path.
    Rover is allowed to traverse the 150mm cube (yellow obstacles) without any penalty on score, however any physical interaction with 300mm cube (green obstacles) will attract penalty points.
    Similarly, rover is allowed to traverse the 200mm diameter craters without any penalty on score; however, any physical interaction with 400mm diameter craters will attract penalty points.

4. Segment 4: Autonomous Sample Drop
    Picked-up sample must be transported to the sample drop position while navigating the obstacles autonomously. Rover must identify the container and required orientation of sample tube for placement. The sample can be        transferred autonomously into the container. Switching to commanded mode during any part of this segment will attract penalty points.

5. Segment 5: Autonomous Final Positioning
    After dropping the sample, rover must come out of ‘FP’ and positioned nearer to ‘FP’ Switching to commanded mode during autonomous final positioning will attract penalty points.
   *there will be no colour coding for the obstacles.

My Insights:-
1. The arena and the task plan has been made to test the rover for the conditions that might simulate the moons conditions on earth's gravity.
2. The first task is to reach from start point to way point by traversing about all the obstacles in between, so there are 3 small obstacles in between, which are 2 15cm side blocks and 1 20cm diameter crater. TO traverse      through both we need to make a system that can do the following:
   i) **Detect the crater and the block**: We have to keep in mind that there is no atmosphere on the moon so the use of something like the ultrasonic sensor will be not viable. So the best alternate we got is using cameras                                            to see the obstacle, use open cv and other machine learning algorithms to help the rover detect the block and craters. Aother good part of using the cameras will be that the                                                   organisers have already told that there will be a well lit environment and we can use computer vision to even know the distance and the dimensions of our obstacles (we have to                                                 read those values as a part of the challenge too).
   ii)**Drive mechanism**: We have to be able to make a drive system that can easily go over a block of sides equal to 15cm and craters of diameter of 20cm. To achieve this we would need to make body with ground clearence                              greater than 30cm to be able to move  over the block or just move aside from the big blocks, no air in the tyres so the tyres do not pop when they are in contact with sharp edges and also we need                             to maintain stability during such traversal. So for that we can make a drive sytem with rubber (for grip) tyres with no air (in earth conditions, we use an air filled zinc coated piano mesh to                                provide rigidity and to avoid  bursting of tyres due to digh speed moon dust). For the stability we may use a 6 tyre mechanism that will raise/descend its legs (by using motors) when moving over                              the obstacles one by one and till then the other 5 wheels will keep the balance of the rover providing it stability which will help us read the surrounding using the camera more easily. The other                             alternative can be using a  very carefully tuned hydraulic supension system for the 6 wheel drive that will be able to easily make the wheel climb and descend over the obstacles. In the whole 1st                             mechanism of drive the camera system has to help us predict that which wheel has to be lifted and when, alternatively for the 2nd mechanism we will need to have tyres of radius upwards of 15cm and                            for both of the cases body will have to have ground clearence in accordance to raise the tyres.
