---
layout: post
title: 'Tesseract'
subTitle: 'Autonomous Event'
logo: /img/event/tesseract/logo.png
actions:
  -
    icon: 'facebook'
    caption: 'Discussion Forum'
    link: https://www.facebook.com/groups/1518258028414691/
  -
    icon: 'youtube'
    caption: 'Tutorial Video'
    link: https://www.youtube.com/watch?v=-z_I5_VtNgQ
  -
    text: 'E'
    caption: 'Event PDF'
    link: '/assets/event/Tesseract.pdf'
  -
    text: 'D'
    caption: 'Do-It-Yourself'
    link: '/img/event/tesseract/diy.png'
  -
    text: 'T'
    caption: 'Tutorial'
    link: '../../tutorial/event/tesseract/'
  -
    text: 'P'
    caption: 'Total prize money worth Rs 45,000'
  -
    text: 'R'
    caption: 'Register'
    link: https://ktj.in/index.php/register
  -
    text: 'F'
    caption: 'F.A.Q.'
    link: '/event/tesseract/faq/'
  -
    text: 'L'
    caption: 'Components List'
    link: '/event/tesseract/components/'
---


#### Introduction

It’s a time fraught with tension for the Avengers, charged with bringing the Tesseract, containing the Space Stone, one of the six Infinity Stones home to safety. The stone’s immense power has attracted hordes of villains and power hungry beings around the universe, who are lying in ambush. It is your job to map out a safe and secure path for Tony Stark to get home with the stone. His life, and the fate of the entire universe, is in your hands!

#### USP

*   Line Following Mechanism
*   RFID Card Reading
*   Path Planning and Optimization


#### Problem Statement

To build an autonomous robot capable of traversing through the arena through a safe and optimized path generated by solving algorithms on data transmitted by RFID cards, to reach the end point.

#### General Description and Event Setup

*   The arena will be a 5x5 grid, with white lines on a black background.

*   Each intersection of white paths, called a node, will have an RFID tag, transmitting integer data.

*   Ambush points around a node means ambush points in the nodes in front, behind, left, right of that node (and above or below too for Round 2).

*   The start node is always safe.

*   In Round 1, the arena will have one level, with each node (intersection of white lines) being a safe or an ambush point.

*   Round 2 is a virtual arena with two levels stacked one on top of the other, aligning perfectly.

*   The data transmitted will be of the format- (number of points of ambush around it on Level 1, number of points of ambush around it on Level 2). For example, 24 at one node means on the 1st level, there are 2 ambush points around it and on the 2nd level, there are 4 ambush points all around it.

*   The maximum possible integer in the above format for Round 1 is 4 , i.e. 4 ambush points around the current node while for Round 2 it is 55, 5 ambush points around the node on level 1 and 5 ambush points around the same node on level 2.
      

#### Arena

##### Both Round1 and Round 2

![](/img/event/tesseract/ktz.png){:.img-responsive}

All dimensions are in cms. 

All RFID cards are placed at a depth of 6mm from the surface on which the arena grid is made.


##### Arena specifications

*   The distance between each node will be 35 centimeters.
*   The dimensions of each node will be 3.5 by 3.5 centimeters.
*   The line width is 3.5 centimeters.
*   The outer dimensions of the arena will be 200 x 200 cm.
*   The dimensions are to be considered with a maximum tolerance of 10%.

##### RFID Card Specifications

*   Universal readable using 13.56MHz RC522 RFID Reader Sensor.

*   “Credit Card” sized plastic white MIFARE RFID Cards with approximate dimensions 82mm x 52mm x 1.4mm.

*   Hint: The Bot can use RFID Card UID for distinguishing between different cards.

##### RFID Card Reading

*   Use this library (https://github.com/miguelbalboa/rfid) for RFID reading. The output of the example code read_personal_data is shown below. The data field of the output will contain the required integer.

*   Details on how to read the data from RFID Cards can be found in our tutorials (https://2020.robotix.in/tutorial/event/tesseract/). The demo code given at the end of the tutorial, will return the value of the integer without having to specify the block number.

![](/img/event/tesseract/24.png){:.img-responsive}

##### Robot Specification

*   The robot must fit in a cube of side 20 centimeters with a tolerance of 10% in its dimensions.

*   No part/mechanism of/on the bot should exceed the given dimensions before the commencement of the event.


##### Event Rules

*   The bot has to traverse the arena using line following mechanism.

*   The initial run can be traversed by the bot in whichever way it so chooses, beginning from the start node, storing data from all the nodes as it goes.

*   Once the bot has traversed the entire arena and reached the diagonal end, it has to display the correct location of all the nodes of ambush found using the data from all the nodes, on an LCD display for a period of 3 seconds per ambush point.

*   The format in which the ambush points are to be displayed on the LCD one after the other is (x, y, z) where x-y coordinate system is marked in the image of the arena above and z coordinate represents the level of the ambush point being displayed.

##### Timeouts and Re-runs

* A maximum of 4 re-runs can be taken. Penalty will be awarded for each re-run and the bot will start from the beginning of the arena. Participants are allowed to make as many changes to the hardware or software as they want.

* A timeout can only be taken in case of a genuine technical fault in the robot. The bot will continue from the same point in that case without making any changes to the hardware or software. Team ROBOTIX can refuse a timeout if the reason does not sound genuine enough, and their decision will be binding and final.
  
#### Round 1

##### Task
*   The arena will consist of 1 level. The bot has to traverse the arena and read the data from the RFID tag on each node.

*   The first round will be characterized into three checkpoints. While traversing the first 6 nodes, the bot will have to read the RFID cards, and display the readings on the LCD display for 2 seconds during which the bot is stationery. This is to check the working of the RFID reader. 

*   After traversing the arena, at the diagonally opposite end point, the bot will have to display all the ambush points in the aforementioned format one after the other for 2 seconds each. This is the second checkpoint, to check the accuracy of the ambush point-finding algorithm.
 
*   From the end point, the bot has to traverse the arena back through a path free of ambush points and reach the start point. This will be the third checkpoint, to check the path planning algorithm of the participants.

*   There is only one safe return path. 

*   In case of the bot failing at any of the checkpoints, the participant will be permitted to take a re-run, the rules of which are mentioned below.

*   The time limit for Round 1 is 7 minutes. Penalty will be awarded for every minute exceeding the time limit.


#### Round 2

##### Task

*   The arena will consist of 2 virtual levels as shown in Example 2 below. The bot has to traverse the arena and read the data from the RFID tag on each node.

*   After the first run, at end point at level 1, the bot will have to display all the ambush points in the aforementioned format.

*   From the end point, the bot has to traverse the arena back through a path free of ambush points on both the levels and reach the start point.

*   Throughout it's return journey, the bot will have to keep either 1 or 2 standard LED(s) glowing representing the level on which it is currently travelling respectively.

*   There will be 2 safe paths, one with higher energy, and one with lower energy, where energy increases with each level. The first level has 20% lower energy than the second level. The bot that travels to the end through a lower energy path will be awarded higher points.

*   The time limit for Round 2 is 5 minutes. Penalty will be awarded for every minute exceeding the time limit.


#### Bonus Round

* Participants wishing to earn some extra points in their final scores after Round 1 and Round 2 can participate in the bonus round described below. This is also the tie breaker round in case of same scores after Round 2.

* The qualifying criteria for making a Bonus Run will be decided after Round 2 by Team Robotix. 

* The arena will consist of 3 virtual levels. The bot has to traverse the arena and read the data from the RFID tag on each node.

* After the first run, at the end point, the bot will have to display all the ambush points in the aforementioned format.

* From the end point, the bot has to traverse the arena through a path free of ambush points and reach the starting point.

* Display the level of traversal using 1, 2 or 3 LEDs.

* There will be 2 paths, one with higher energy (where higher energy refers to using more nodes on the higher levels and every level has a 20% increase in its energy), and one with lower energy.

* The paths will have different number of segments (distance between two nodes ) and different number of turns.

* The bot has to traverse the arena using the lower energy path, or the fastest path (with lesser number of segments), depending on the total number of ambush points. If there are an odd number of points, the fastest path should be taken, and vice-versa.


##### Scoring Formula

* **Positives**

* Base score - 500
* Line following - 200
* Checkpoint 1 (Display of first 6 RFID Readings) - 100
* Checkpoint 2 (Detection/display of each correct ambush point) - 200
* Each safe node traversed while returning - 50
* Checkpoint 3 (Successfully returning to the start point through the safe path) - 100
* For traversing the lesser energy path (Round 2) - 200

* **Negatives**
* For each ambush point touched while returning - 50
* For each re-run - 100
* For each timeout - 50
* For every minute exceeding the time limit - 100
* For damaging the arena - 400

* **Example 1:**

Round 1 trial demonstration for a 3x3 arena-

*   Readings from RFID Tags:
![](/img/event/tesseract/ex11.jpg){:.img-responsive}


*   After analyzing and solving the readings from RFID, the nodes of ambush points are shown below.
*   Row, Column indices displayed by the bot on the LCD display before the return journey: (0,1), (1,2), (2,0).
![](/img/event/tesseract/ex12.png){:.img-responsive}

*   Return path safe from the ambush points followed by the bot in the return journey:
![](/img/event/tesseract/ex13.jpg){:.img-responsive}

* **Example 2:**

Round 2 trial demonstration for a 5x5 arena-

*   Imaginative view of the two levels of Round 2:
![](/img/event/tesseract/ex21.JPG){:.img-responsive}


*   Ambush points on the lower level:
![](/img/event/tesseract/ex22.JPG){:.img-responsive}

*   Ambush points on the upper level:
![](/img/event/tesseract/ex23.JPG){:.img-responsive}

*   Bot traversal after detection of ambush points and path planning:
![](/img/event/tesseract/ex24.jpg){:.img-responsive}

       ![](/img/event/tesseract/ex25.jpg){:.img-responsive}

       ![](/img/event/tesseract/ex26.jpg){:.img-responsive}


##### General Rules

* Maximum number of participants allowed per team: **4 people**.

* The participants will be provided with **220 Volts, 50 Hz** standard AC supply.

* Only **16 bit** microcontrollers or below will be allowed.

* Participants will have to arrange for any other power supply required for their robot.

* Teams cannot tinker with their robots during the run.

* [LEGO kits](http://en.wikipedia.org/wiki/Lego_Mindstorms) or its spare parts are not allowed.

* The decision of the Team Robotix will be **final** and **binding**.

* The rules are subject to change.

It is suggested to the participants to try making a wireless robot, powered by a battery on-board.

**Links to Tutorials:**

For relevant tutorials check [ROBOTIX TUTORIALS](https://www.robotix.in/tutorial/).

##### Contact

###### Manthan Patel

Email: **[manthanhemangpatel@gmail.com](mailto:manthanhemangpatel@gmail.com)**

Ph. no: **+91 9033034268**

###### Anirudh Roy

Email: **[royanirudh99@gmail.com](mailto:royanirudh99@gmail.com)**

Ph. no: **+91 9891877561**