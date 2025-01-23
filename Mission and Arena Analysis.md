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






