# Mobile robotics -jimenade
## 1st proyect
The assignment for this 1st project is to program an autonomous vacuum in python, only using the laser to detect objects the vacuum has.
I did this project using the website Unibotics, which has the screen divided in 4 parts, the 1st one is de left and up corner, where you can write the code, the left down is a terminal window,like Unix terminal, the right up corner is a map of the house, and the last one, the right down corner is like an external camera to see what the robot does.
The libraries I am using for this project are: 
* GUI
* HAL 
* math
* numpy
* random
* time

I decided to do a while loop to read all the time the distance values of the laser, and if any value of the range I decided to read is smaller than 35 cm or 0.35 m (this is checked with a for loop) then turn and randomly(aprox 30% of the time) the robot starts doing a spiral movement until it founds an obstacle.

At the begining I chose to read the laser distance values in the 75º to 105º range so the vacuum could sense 30º in front of it, but then I realized with those values the robot got stucked easily in the chairs, the coffee table in the dinning room and with the tables beside the bed.
So for solve that problem y decided to change the range, so now my vacuum sense form 65º to 115º, in total 50º.
For preventing get stucked I also decided that the spiral movement and the turn shold have opposite turning direction, the turn is to the left and the spiral turns to the right.

- For the turning I used a random time between 0 and 0.5 secs to turn.
- For changing the modes of the robot (forward, turn and spiral) I created a function where the new state is the param and with nested if-else the vacuum chooses what to do.
Doing the things i said before my robot vacuums around 70% of the house in approximately 20 minutes.
![image](https://github.com/jimenade/rob.movil-jimenade/assets/102520569/ab94f4b0-ff1d-4e6d-88a2-3ea34a8ce77a)
