Introduction: There were multiple rovers that were participating in the IRoC-U 2024' and out of those only 20 teams were qualified to participate in the field round. In the previous document I have analysed 3 rovers from 3 different top 10 teams and in this document I will be pointing out problems that each team has in the systems and what can be the possible solutions of all those problems.

Contents:

1.Team Obseract - Jadavpur University

    1.1.Tyres
    1.2.Antenna used
    1.3.Suspension.

2.Team Samarth - Sharda Unviersity

    2.1.Tyres
    2.2.Use of Ultrasonic Sensors

3.Team Shunya - IIITD Kancheepuram

    3.1.Drive
    3.2.Suspension
    3.3.Manupilator placement
    3.4.Manupilator camera placement


1. Team Obseract - Jadavpur University

1.1.Tyres: 

Problem: The tyres used by team obseract are good enough to their job but could have been way better. THe tyre design that they desided on was smoother than what was needed, making the tyres sometimes slip while the rover was turning using diffrential drive mechanism.

Solution: This problem can be solves simply by designing a wheel design with more frequency of cleats and thinner but longer cleats, something like what Team shunya used. The new design will reduce slipping of tyres in M-Sand drastically, which will result in more efficient movements, which do not load the PID that much and helps the rover in making much more precise movements.


1.2.Antenna used:

Problem: The team has used the ubiquiti litebeam M5 antenna for the connection with the groundd station, but the use of this is an overkill as it has a range of 30 km + whereas we need connectivity till 20m minimum, and occupies more volume. The antenna weighs about a kilogram, removal of which might not bring a very significant change in the ynamics of the rover, but will surely be benificial for the rover.

Solution: The team can use any normal transmitter reciever system which is not built for large range communications. They can use the following configuration:-

-The video feed transmitter reciever system: transmiter:TS832 FPV transmiter, Reciever: RC832. This transmiter reciever pair is mostly used in FPV drones and show a very low latency feed.

-For data transmission: NRF24L01 PA LNA trans reciever module which operates on 2.4 GHz frequency.

This configuration was used by Team Samarth and was very compact. Other teams can be seen using other transmitter reciever pairs but not as big as used by the Team obseract.

1.3.Suspension:

Problem: The team uses a rocker-bogie suspension system but the rover still fall from the block freely, which migh be calculate as a jerk by the IMU which and also may interupt in mapping of its surroundings.

Solution: This problem too was solvedd by Team Samarth as they used 4 small passive hydraulic suspensions which smoothen the fall of the robot and hence makes the overall suspeension just better. This is not a very serious problem but still would be a really good improvement.


2. Team Samarth - Sharda University

2.1. Tyres:

Problem: In this rover too tyres are a real problem, the team uses thin tyres which are known to be bad for rough terrains due to their smaller contact with the groun hence leaing to less traction, also the wheels are not continous, so there will be situations in which the corner points of a wheel will have to bear more load than the others, which causes damage to the tyres.

Solution: The tyres should be a bit more wider, just like the ones of team obseract and the discontinous circumference might be kep but it must be ensured that even the corners of each section are directly connected to the centre of the wheel and the material usedd should be able to bear such load.

2.2.Use of ultrasonic sensors:

Problem: Even though the competition is set in the earthly environments we cannot ignore the fact that the challenge is inspired from the lunar missions, where the ultrasonic sensors would be useless due to the lack of an atmosphere good enough to send sound waves.

Solution: The most simple solution to this problem is the use of infrared sensors in the place of ultrasonic sensors.



3. Team Shunya - IIITD Kancheepuram

3.1.Drive:

Problem: The team uses a steering drive rather than a diffrential rive to turn the robot, this is bad as in the sandy terrains with the thick tyres, it gets real hard for the rover to turn its tyres, ad due to the precision factor the rover has to stop an then turn in the arena rather than steering while moving just like in cars.

Solution: In a rover like this the diffrential drive is the best method to traverse with the thick spiky tyres. This would also save the team the headache of attaching the gear system, fitting well in the volume requirments and would save them some cost and will help them get more comfortable with the weight requirments.

3.2.Suspension:

Problem: The triple bogie suspension is a unique pick and is not suitable for the situiation of this challenge. The Triple-Bogie suspension system is know for its weight balance and distribution capabilities, hence it is used in trucks which have to carry enormous load, but the challenge ddoes not require carrying of heavy load, and alot of weight of the rover is addded below the suspension system by its bulky wheels an their steering mechanism. 

Solution: The use rocker-bogie suspension would be ideal for this robot as it woul cut their cost of extra material and help in weight redduction of the rover, would perfect to traverse in such a plane with the tyres of choice. The tyres of the rover a re bulky and heavy, making them fall with a higher jerk, to counter this, we can use extra suspensions like hydralic or sping type suspensions to smoothen the fall of the wheels.

3.3.Manupilator placement:

Problem: The manupilator is a big component on the face of the rover and it may obstruct the stereo camrea which helps the mapping of the arena, the manupilator being in the frame may be prroblematic for the mapping.

Solution: The manupilator must turned to an extreme side, making it go out of the frame of the camera. This problem can be countered by proper scanning of the surrounddings by constant turning too, but that process will surely eat up time.

3.4.Manupilator camera placement:

Problem: The manupilator's camera is placed on the gripper part rather than the body of the rover, this makes the camera constant moving and prediction of where to close the claw way harder.

Solution: Putting the camera to the rover's body will make it easier for the system to pickup and drop the sample target as then the algorithm will have to just match the centre of the gripper of the manupilator and the centre of the tube and would make the process more accurate and faster.
