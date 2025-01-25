Introduction:
ISRO wants to progress into the fields of artificial intelligence and machine learning and space robotics as it looks forward to its ISRO in-orbit servicer mission, Lunar sample return mission, space docking mission, etc..All of these steps are natural after the succes found by the Chandrayan 3 mission. As a plan for further progress ISRO had decided to launch the ISRO robotics challenge 2024 where they motivate students to give innovative ideas and prototype them which can perform specific tasks in conditions similar to the lunar surface. These solutions to problems faced by the rovers right now have high chances of being implemented by ISRO in their next missions.

The objectives of this challenge are to:-
1. provide a platform for exploring the domain of space robotics.
2. To help the students increase their critical thinking and problem solving skills related to the areas of space robotics.
3. To develop innovative solutions for the future of ISRO.
The challenge is designed in such a way that is inspired by the extra-tereestrial conditions and hence forces students to solve problems that are originated in real missions too, and hence the competitors are forced to use all of their problem solving in order to find the most economical ways to finish the tasks.

In this document I will be analysing the arena, rules and task and finding possible ways to approach the problems given to us.

Contents:-

1.Qualifier Round

    1.1.Arena described for the qualifiers round
    1.2.Rover and Manupilator requirements (same for all the rounds)
    1.3.Tasks to be performed in this round
    1.4.My insights on how can we achieve these tasks

2.Field Round

    2.1.Arena described for the Field round
    2.2.Rover and Manupilator requirements (same for all the rounds)
    2.3.Tasks to be performed in the Field round.
    2.4.My insights on how can we achieve the given tasks.

3.What can be done overall
   
    3.1.Sensing
    3.2.Drive
    3.3.Manupilator
    3.4.Communication
    3.5.Algorithms
    3.6.Computer
    3.7.Efficient algorithm/ plan of action
    

**For the Qualifiers round:**

Arena:
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

I. **Detect the crater and the block**: We have to keep in mind that there is no atmosphere on the moon so the use of something like the ultrasonic sensor will be not viable. So the best alternate we got is using camera       to see the obstacle, use open cv and other machine learning algorithms to help the rover detect the block and craters. Aother good part of using the cameras will be that the organisers have already told that there          will be a well lit environment and we can use computer vision to even know the distance and the dimensions of our obstacles (we have to read those values as a part of the challenge too). We can use sterero vision(2         cameras) or give the rover obstacles preknown dimensions as reference to measure the distance from the rover.

II.**Drive mechanism**: We have to be able to make a drive system that can easily go over a block of sides equal to 15cm and craters of diameter of 20cm. For this we can use many suspension systems such as the positive         and negative quadrilateral levers suspension mechanism which is excellent for climbing over obstacles (220mm considering frictional constants of moon surface and does not need the wheel's radius to be bigger than the       obstacle), smooth travelling, equal distribution of load to all 6 wheels and can be folded easily for easy carrying or maybe use the rocker bogie system that can climb upto 20-30cm obstacles (much simpler and hence         better for this case).

III.**Turning**: We should use a diffrential drive system for such a project as that is much easier to use and avoids using extra motors to turn.

3.The second task is to identify and pick up the sample, so for that, as we can already set the path of the rover we may not use a rotating camera and the camera can detect the distance between the target sample and us,      then we can use the manupilator to pickup the sample, the manupilator needs only 2 degrees of motion if our diffrential drive is good enough and would need 1 degree to descend/ascend and the other to approach/distance      the target sample .

4.Now we need the rover to navigate the terrain automatically to the sample drop point. For the detection of where the drop point is we may need a camera up high (under the height limit) which will scan the surroundings       and identify where the drop point is. Next the rover must identify the obstacles in between itself and the blocks, and choose the most efficient path considering its ability to traverse through different types of            obstacles.

5.Next when the rover has reached in the drop zone (1500mm diameter circular region), we may use the cameras to identify the blue tube and use algorithms that approach the drop point and use the arm to drop the sample         target.

6.Final task for the robot is to come out of the final point (1500mm diameter circle) and position itself nearer to the final point autonomously, which can be done by measuring disance from the the tube to know that we are out of the final position zone and also keep in mind of the obstacles that might be in its surroundings.

For the field round:-

Arena:
1. Size of the arena: 12 m X 9 m.
2. Known elements in the arena:
 a) 4 m dia. traversable crater with a depth of 200 mm and the slope of the rim is < 15˚
 b) 2.5 m dia. traversable hump with a height of 260 mm made up of M-sand
 c) Hard terrain
 d) Non-traversable wall of height of 0.8 m
 e) Traversable slot with a length of 1.8 m, width of 0.6 m and depth of 100 mm
3. Filling material of arena: M-Sand (100 mm depth)
4. Entry Points: 2 Entry points are provided with different difficulty levels. Team can choose any point as per their rover capability. Choosing difficult entry (entry-1) will have more scoring weightage. Please refer         section 4 for scoring criteria. Width of entry point will be nearly 1.5m.
5. Sample: In total, 3 samples will be present in the arena at three different locations with different difficulty level. A rover can pick any number of samples in the given time.
6. Identification Markers: Few bonus markers will be placed in the arena at random locations. The locations may vary for each team. Bonus markers will be coloured and star-shaped.
7. Traversable Obstacles: Obstacles of random shape/sizes (the size of the sample will the limited within 150x150x150 mm) will be distributed within the arena at unknown locations.
8. Non-traversable obstacles: These obstacles of random shape/size (300x300x300 mm > x > 800x800x800 mm) will be placed randomly. These obstacles are meant to be avoided. There is no limitation in the size of these obstacles
9. Craters: Craters are created at random locations and depth of the craters will be limited within 200 mm.
10. Hard Terrain: Hard surface without any M- Sand will be present within arena which is traversable and it will be flushed to m-sand height.
11. Exit Points: 2 Exit points are provided. Team can choose any point as per their convenience. Choosing exit-1 will fetch more weightage of marks
12. Boundary: 200 mm boundary edges will be provided and marked with yellow paint for clear demarcation
13. Separation between any two non-traversable obstacles will be maintained more than 1m.
Note: Number and coordinates of traversable obstacles, non-traversable obstacles and craters will not be disclosed.

Rover and Manupilator requirments: Same as qualifier round

Tasks:
Task-1: Autonomous Navigation Task:
The team is required to design and demonstrate the performance of rover’s navigation by traversing from entry point to sample collection point (of the choice the team) and subsequently to the container point and then exit from one of the identified locations. Rover can traverse in any path. The teams are allowed to give maximum 4 commands if required in the total task at the following checkpoint which are as follows:
1. At the start of the task (at entry point-1 or 2)
2. After the drop of first sample
3. After the drop of second sample
4. After the drop of third sample
Following navigation tasks needs to be performed:
a) Entry: The team can choose from two available options. Entry-1 will fetch more points.
b) Obstacle identification using sensors: The sensors shall be capable of identifying the dimension of the obstacles and take appropriate decisions.
c) Craters identification using sensors: The sensors shall be capable of identifying the size of the craters.
d) Sample location identification: OD 80 mm, L 125 mm (approx.) red in colour
e) Container location identification: A cylindrical container of diameter 150 mm and height 150 mm, which is placed at the target location, needs to be identified
f) Locations of the sample tubes (centre axis):
1. Sample Tube-1: (3.5 m, 6.5 m) – placed inside the 4 m traversable crater
2. Sample Tube -2: (9.9 m, 1.35 m) – placed on the 2.5 m traversable hump
3. Sample Tube-3: (8 m, 6 m) – placed on the hard terrain
g) Locations of the sample container (centre axis): (11.5 m, 8.3 m)
h) Exit parking:
1. Exit-1 position: 1.5 m x 1.5 m square with a centre of (11.3 m, 4.35 m)
2. Exit-2 position: 1.5 m x 1.5 m square with a centre of (8.83 m, 8.3 m)
Note: The sample tube, container and exit locations coordinates can have ± 0.5m variation from the above-mentioned coordinates
i) The boundary will be marked with yellow for clear distinction. The entry and exit boxes will be marked with white boundaries
![image](https://github.com/user-attachments/assets/41ae67b6-8889-4f53-b462-a81f041accfe)

Task-2: Autonomous Sample Picking and Placing:
a) The sample pick and-place task needs to be accomplished by a manipulator arm mounted on the chassis.
b) Target identification using visual sensors: A tube which represents sample to be collected forms the target for the Rover. Following are the details of the sample that needs to be identified successfully before being picked up:

Details of sample (tube):
![image](https://github.com/user-attachments/assets/23b69346-2018-44e2-af3f-387bf29b07ef)

Details of sample container:
![image](https://github.com/user-attachments/assets/dd37d4d8-81be-4ea3-a2b9-19875138d84f)

c) Picking and securely holding the sample: The sample tube needs to be picked up from the surface using a gripper. The sample then needs to be held securely by the rover before mobility is initiated.
d) Unloading and placement: The rover needs to approach and unload the sample into the cylindrical container.
e) After each drop of sample tube in the container it will be removed from the container, making place for the next sample tube.
f) Picking and Dropping of each sample is an independent event and rover should handle only one sample at any point of time.
Note: The sample tube can be placed in any orientation at its designated location

Task-3: Repeat the Task-1 & Task-2 until all the samples are dropped in the sample container:
The rover needs to repeat the Task-1 & Task-2 until all the samples Are dropped in the sample container. Only change is the rover will be at sample container location after drop of 1st sample and 2nd sample.

Task-4: Identification of specific markers:
Identification of bonus targets includes the following:
1. Capturing its images/shape with some sensor.
2. All the bonus targets are marked with distinctive number and the team also needs to identify the number
3. Coordinates of the particular bonus target to be identified with a variation of ± 0.5m
   Details of the Bonus Marks:
   ![image](https://github.com/user-attachments/assets/811d1a36-5e92-4281-b69c-e5bb3612765e)

The full marks for the identification of bonus marks will only be allotted if a proof of detection and allotted number are provided along with coordinates. However, a partial mark will be given if all the requirements are not satisfied.

My insights:
1. In this stage we will be given the coordinates of the points where the sample tubes are, where the big ditch is, where the sand hill is and where the drop point is. So we would not need a any camera to scan and detect the drop point and only one camera would be enough to detect the obstacles, sample tubes and the drop point.
2. The drive mechanism as the same would be good enough to support the tasks in this round, just we owuld need motors that have high torque in order to climb over 15 degrees of elevation.
3. The robot will just move towards the point it wants to go, just if any untraversable object comes in front of it , it will just avoid it and keep doin that until it reaches to the desired points and it will also map the obstacles each times it encounters them in order to optimize its path in the further navigation.
4. The mechanism used to accurately pick up the sample tube and drop it will be the same.
5. The bonus marker's image will be preprocessed in the system hence it will be detected whenever it encounters the bonus marker and register its photo and other information in the system.

**What can be done overall:-**
1.For Sensing and Seeing Objects: sensing and seeing objeets can be done by the following methods and would be used after seeing their accuracy, cost and effectiveness:-

I.Camera: We can use AI training models and openCV to see the area around us just like the humans and map the area around us, this can be used to identify colour of the sample tube too. Camera is a must for perfect identification of the sample tube and the drop point. Camera can very easily be cheap, its accuracy is based on the accuracy of the trained AI model to map its surroundings and would be very effective.

II.Lidar: Lidar is a very expensive solution of this problem but it will map out the surroundings pretty well, but still it will need a camera to identify the colour codes and will not be very efficient.

III.IR Sensor + Camera: we can use this combination we find trouble in finding distances of the objects from the robot but still it would not be able to help with detecting the dimensions of the objects, hence making the use of IR sensor pretty redundant.

Hence we can be sure that the use of Cameras with a properly trained openCV AI trained model will be the easiest and the most cost effective way to detect the sample tube and drop points along side the obstacles.

2.For Driving: For driving we should be using diffrential drive as it uses the least amounts of motors for turning and is very simple to program. We should use a Rocker-bogie suspension system for its simplicity and ability to satisfy the tasks given successfully.

3.Manupilator: We will need a manupilator with 2 degrees of freedom which will be:-

I.The Degree which will make the arm approach and distance from the target, this would be like our elbow joint.

II.The degree which will look on the arm goin up and down, this would be like our shoulder.

We would not need anything like the wrist as the drop point is wde enough to let the sample tube drop lengthwise. This is considering a decent driffrential drive system, or else we would need another degree of freedom to move the arm sideways to ensure an accurate picking and droping of the sample tube.

4.Communication: As specified by the rule book, we must use radio signals for any communication with the robot and the radio frequency needs to be legal to use.

5.Algorithms: The algorithms will have to be such that they keep moving  maping the map and try to find the path with the least no. of non traversable obstacles to complete the task faster. The unmapped obstacles would be mapped upon each encounter and the path mus update according to the new map.

6.We need tyres which would have incredible grip or have discrete circumference to be able to move easily throught the sand and also be able to climb the sharp edged 15cm block.

7.Computer: We would need a computer that can run good algorithms and not be very costly.

8.What the most efficent algorithm should do:-

I. Qualifier round: The robot will easily navigate throught the small obstacles as per the pre input path till the way point, at the way point the camera at front will work upon picking up sample tube with the help of manupilator, and the camera installed at the top will be scouting for the blue drop point. When the drop point is identified, we shall where the other large obstacles are and see if nonne are in the direct path, if there are none then the robot should move straight to the drop point after turning keeping in mind that its sides must not be touching the untouchable obstacles and would be identifying the traversable obstacles whenever they are encounterd. Now the rover shall drop the sample tube again using the combination of its camera and the manupilator. At the end the rover shell back up to the path it took previously just enough that it is out of the final position circle.

II. Field Round: To fetch more points we shall take entry from the entry point 1, then the robot shall compute that approaching which sample tube would be easiest for it at first, we need to keep in mind that we do not need to take traversable slot as there are no points added to traverse through it hence it would be easier for the robot to leave from the other side of the untraversable wall and then just move down the ditch, fetch the tube and run for the drop point keeping the traversable and untraversable in consideration. The rover shal also remember that there would be a gap greater than 1m between 2 untraversable obstacles, so it should ot just change direction after encountering any untraversable obstacle but always look for the turn after 1m. We may need 2 camera setup for this round too, so the camerab below should be always lookin gofr the bonus markers while the the upper camera should be watching out for the untraversable blocks. If the bonus Markers are not found even after completing the droping of all 3 tubes and there is some time left then we shall use that time to run around and look for those markers, but the rover must be able to estimate the time it would need to exit from its position, and must abort the mission of finding bonus markers immediately after the time left is too less.
