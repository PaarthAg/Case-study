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
   1. **Detect the crater and the block**: We have to keep in mind that there is no atmosphere on the moon so the use of something like the ultrasonic sensor will be not viable. So the best alternate we got is using camera       to see the obstacle, use open cv and other machine learning algorithms to help the rover detect the block and craters. Aother good part of using the cameras will be that the organisers have already told that there           will be a well lit environment and we can use computer vision to even know the distance and the dimensions of our obstacles (we have to read those values as a part of the challenge too). We can use sterero vision(2          cameras) or give the rover obstacles preknown dimensions as reference to measure the distance from the rover.
   2.**Drive mechanism**: We have to be able to make a drive system that can easily go over a block of sides equal to 15cm and craters of diameter of 20cm. For this we can use many suspension systems such as the positive         and negative quadrilateral levers suspension mechanism which is excellent for climbing over obstacles (220mm considering frictional constants of moon surface and does not need the wheel's radius to be bigger than the        obstacle), smooth travelling, equal distribution of load to all 6 wheels and can be folded easily for easy carrying or maybe use the rocker bogie system that can climb upto 20-30cm obstacles (much simpler and hence          better for this case).
   3.**Turning**: We should use a diffrential drive system for such a project as that is much easier to use and avoids using extra motors to turn.
3.The second task is to identify and pick up the sample, so for that, as we can already set the path of the rover we may not use a rotating camera and the camera can detect the distance between the target sample and us,       then we can use the manupilator to pickup the sample, the manupilator needs only 3 degrees of motion if our diffrential drive is good enough and would need 1 degree to descend/ascend and the other to approach/distance the   target sample and the last one to rotate the sample in order to fit it in the tube as the tube is in a vertical orientation.
4.Now we need the rover to navigate the terrain automatically to the sample drop point. For the detection of where the drop point is we may need a camera up high (under the height limit) which will scan the surroundings       and identify where the drop point is. Next the rover must identify the obstacles in between itself and the blocks, and choose the most efficient path considering its ability to traverse through different types of            obstacles.
5.Next when the rover has reached in the drop zone (1500mm diameter circular region), we may use the cameras to identify the blue tube and use algorithms that approach the drop point and use the arm to drop the sample         target.
6.Final task for the robot is to come out of the final point (1500mm diameter circle) and position itself nearer to the final point autonomously, which can be done by measuring disance from the the tube to know that we are out of the final position zone and also keep in mind of the obstacles that might be in its surroundings.




