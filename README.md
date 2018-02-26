# Arduino Maze Solver

  This program solves a maze using the idea of following a specific wall in order
to find the exit. It is capable of solving a maze with a single T-Junction and
and any number of other turns/dead ends.

# Component List

- BOE-BOT from Parallax : https://www.parallax.com/product/boe-bot-robot
- Arduino Nano 
- HC-SR04 Ultrasonic range finder (x3)
- HMC5883L Compass Module
- SSD1306 OLED Display (128x32)
- AT42QT1010 Capacitive touch sensor (Any old momentary switch will suffice)
- Custom printed PCB
- Custom printed sensor bracket

# Basic Operation

  This program will perform 3 runs of the maze. 2 of these runs are to determine 
which direction the robot should turn at the T-Junction during the final run of
the maze. This allows the robot to solve the maze quickly on all runs due to the
decision on which route to take is already chosen. However this would encounter
issues when more T-Junctions are added but is more than sufficient for this type 
of maze.
  The code can be continued after every run by pressing a push button which allows
the user as much time as required to replace the robot at the start of the maze.
However since the timings of the maze are only stored in RAM, the robot is required
to be on throughout the whole process (ALL 3 RUNS) or the process will have to be 
restarted due to the timings being lost.
