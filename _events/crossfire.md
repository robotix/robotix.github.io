---
layout: post
title: 'Crossfire'
subTitle: 'Manual Robotics Event'
logo: /img/event/crossfire/logo.png
image: img/sections-background/crossfire_black_layer.png
actions:
#   -
#     icon: 'facebook'
#     caption: 'Discussion Forum'
#     link: https://www.facebook.com/groups/1518258028414691/
#   -
#     icon: 'youtube'
#     caption: 'Tutorial Video'
#     link: https://www.youtube.com/watch?v=-z_I5_VtNgQ
  -
    text: 'E'
    caption: 'Event PDF'
    link: '/assets/event/Crossfire.pdf'
#   -
#     text: 'D'
#     caption: 'Do-It-Yourself'
#     link: '/img/event/tesseract/diy.png'
  -
    text: 'T'
    caption: 'Tutorial'
    link: '../../tutorial/event/crossfire/'
  -
    text: 'P'
    caption: 'Total prize money worth Rs 50,000'
  -
    text: 'R'
    caption: 'Register'
    link: https://ktj.in/#/event/Crossfire
#   -
#     text: 'F'
#     caption: 'F.A.Q.'
#     link: '/event/tesseract/faq/'
  -
    text: 'L'
    caption: 'Components List'
    link: '/event/crossfire/components/'
---


#### Introduction

<p style="text-align: center">
<em>“If you were waiting for the opportune moment, that was it.” -Jack Sparrow
</em>
</p>

Two ships, one led by an exceptional pirate captain Jack Sparrow, the other raging through the seas under the command of Blackbeard. Who do you think will come out on top? Be a part of the battle yourself to find that out!

<!-- #### USP

*   Line Following Mechanism
*   Colour Recognition
*   Memory and backtracking -->


#### Problem Statement

To build a robot having dimensions within the specified range and capable of **playing with the ball, avoiding opponent bots and obstacles**.


#### USP

*   Differential Drive Mechanism
*   Remote Control Mechanism
*   Dribbler/Kicker Implementation


#### Event Rules

*   The arena is a hexagon-shaped football field divided symmetrically into 6 triangular areas, with each side of the hexagon having a goalpost in the middle.

*   A solid round ball will be used for the game, weighing approximately 50 gm and a diameter of 4.5 cm (0.1476 ft).

*   At the beginning of every match, teams have to choose the three goalposts that they will be defending. 

*   Following is the process for it:
    1.  Coin tossed once. The winner gets to choose 1 side, the loser then chooses another.
    2. The above coin toss is done two more times and hence, each team gets three goalposts at the end.

*   Before the beginning of each match, the ball will be placed in the central area, and the two bots will be placed in their assigned positions.

*   The main aim of the participants is to shoot the ball into any of the opponent’s goalposts. The ball should only be taken across the field by pushing and kicking. 

*   Some obstacles will be permanently fixed on the arena. Besides this, each player will get a few obstacles to place on the arena in their half strategically.

*   Here, their half comprises the three triangular areas corresponding to the three goalposts that they are defending.
Obstacles are for blocking the path of the ball/bot, and touching it would not lead to any penalty.

*   Obstacles are for blocking the path of the ball/bot, and touching it would not lead to any penalty.

*   After half-time, the teams will switch their goalposts, and the game proceeds without any change in the position of the obstacles.


#### Arena

##### 3D representation

![](/img/event/crossfire/arena_3d.png){:.img-responsive}

##### Top view

![](/img/event/crossfire/arena_2d.jpg){:.img-responsive}


##### Arena description

*   Length of Hexagon side: 6 ft (182.88 cm)
*   6 goal posts at 6 sides.
*   Length of the goal post = 1.476ft (45 cm).
*   A wall of height 25cm (0.820 ft) encloses the battlefield.
*   Obstacle Dimensions = 10cm x 10cm x 10cm.
*   Obstacles will be stuck by the team using velcro at the beginning of the game (taking care that there is sufficient space for the bot to pass through). However, once the game has started, it cannot be changed.
*   The organising committee will provide obstacles.
*   There will be a rectangular area around the goalpost as well as a central area which will be free of obstacles.
*   All these dimensions are dynamic and are subject to slight changes which will not affect the robots already made by the teams.


##### Robot Specification

*   Size must be within length = 25 cm(0.820 ft), width = 25 cm(0.820 ft), height = 25 cm(0.820 ft) with a tolerance of 10%.

*   The wires should be bound into a single strand. Furthermore, a fixture is to be added such that wire comes out of the top of the robot.

*   Maximum weight = 3 kg with a tolerance of 10%.

*   The bot may have a kicking/shooting mechanism, but the extension should not increase the length/width of the bot by more than 5 cm (0.131ft).

*   For the driving mechanism, the group can use a maximum of 4 motors. However, additional motors can be used for a kicker, striker, dribbler, etc.

*   The bot must not have any mechanism or part that holds/grabs the ball.

*   The bot will undergo a screening by the organising team before every match. The decision of the organising committee will be final in this regard.

*   Any violation of these rules will constitute immediate disqualification from the event.


##### Debugging and Timeouts

*   Each team has the option to call for a time-out twice during the entire match for the case of debugging.

*   This timeout will only be allowed if the bot is incapable of locomotion and cannot resume working without human intervention.

*   After debugging, the bots and the ball will be kept at their original positions, and the game will continue.

*   In case of wires get entangled, the referee will call for a timeout, and the wires will be disentangled. In case any team is found to be doing it on purpose, the team will get one warning, after which repetition of this foul will lead to the disqualification of the team.

*   The final call on all decisions, including whether the team will be given a timeout and disqualification of teams, will be of the referee.

  
#### The Tournament

The plan for this section is dynamic and is subject to change.
In all cases, the decision of the organising team would be considered final and binding.

##### Knockout Stage

*   All the teams will be set to have a match in groups of two.

*   The winner of each match will qualify for the next round, and so on.

*   A total of 12 teams will qualify for the group stage from the knockouts.


##### Group Stage

*   The teams will be divided into 2 groups (leagues) with 6 teams each.

*   The top two teams of each league will advance to the semi-finals.


##### Semi-Finals

*   If the top two teams of league A and league B are A1, A2 and B1, B2 then there will be a match between A1 and B2 and similarly between A2 and B1.

*   The winner of these two matches will go to the finals.

*   The teams which lost will now play for 3rd place. 


##### Finals

*   The 2 teams left standing will fight in a **Football Stand-Off** for the title.


##### Scoring System

*   Each match will go on for a maximum of 8 minutes, with a half-time of 4 minutes.

*   At the beginning of the game, each team(with three goalposts) will have to assign 2 points to one of their goalposts and 1 point to the remaining two.

*   After every goal done by any team, the match timer stops and the position of the bots and ball will be reset.

*   During any match, if the duration of 8 minutes is over and there is a case of a tie, an extra time of 2 minutes will be provided.

*   Even after these 2 minutes, if there is a draw, then the team with the highest number of 2-pointer goals will be declared the winner.

*   If even the 2-pointer goals are equal, then the match continues until the first goal. The team that makes this goal wins.


##### General Rules

* Each team must consist of 1 to 4 members.
* Every participant must be a part of only one team.
* The use of LEGO kits or ready-made bots will lead to disqualification.
* Only one bot is allowed per team, and only one team member can control the bot during the entire duration of a particular match.
* Sportsmanship is expected from the participants.
* Damage to the arena or the obstacles in any form will lead to immediate disqualification.
* The organisers reserve the right to change the rules as they deem fit. Changes, if any, will be notified to the participants.
* Team Robotix’s decision will be final and binding.


**Links to Tutorials**

For relevant tutorials check [TUTORIALS](/tutorial/event/crossfire).

##### Contact

###### Tanmay Mohanty
Head, Technology Robotix Society

Email: **[tanmay.mohanty18112002@gmail.com](mailto:tanmay.mohanty18112002@gmail.com)**

Ph. no: **+91 9002921996**

###### Yashi Gaur
Head, Technology Robotix Society

Email: **[yashigaurbcgs@gmail.com](mailto:yashigaurbcgs@gmail.com)**

Ph. no: **+91 9886624125**