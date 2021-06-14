**Raspberry Pi Automated Plant Watering with Website**

**source**: https://www.hackster.io/ben-eagan/raspberry-pi-automated-plant-watering-with-website-8af2dc

**Aim**: To read mositure lvl of soil and water it when needed

**Material**:
Raspberry Pi, Relay, 3-6v Submersible Pump, Flexible Water Line, SparkFun Soil Moisture Sensor (with Screw Terminals)

**Details**: 
As the title and aim suggest, we want to set up Raspberry Pi so it can take reading of moisture and run pump when mositure lvl is low. we will first put the moisture senser in plant soil and connect the sensor with Raspberry Pi as shown in figure. All other part is also connected as in figure.
![image](https://user-images.githubusercontent.com/85681011/121859773-c0590980-cd15-11eb-97a7-9f5183928505.png)

**working**:
This resistance is inversely proportional to the soil moisture: so when moisture decrease, resistance will increase. Raspberry pi will take this value as input and when it exceddes a certain value (which tell water moisture is less), Pi will pass high voltage to relay which will result the circuit of power source and pump to complete. Hence pump will start and will supply water to plant till resistance decrease in moisture sensor







**Creating and Solving Mazes on a 128 x 64 LED Panel**

https://www.hackster.io/doug-domke/creating-and-solving-mazes-on-a-128-x-64-led-panel-bb7740

**Aim**: Generate a random maze and then solve it

**Material**: Arduino Due, 64 by 32 LED panel, 5 volt 20 amp Power Supply, jumper wires

**About project:**
This is a coding focus project where we want to create a random maze with a unique solution - have unique random point of escape, on LED display amd then solve it. To create maze we implement regressive backtracking algorithm which mainly use the concept of stack and heap. 

**Creating Maze:**
To create maze, we will create an empty stack of list of cells. Then we will choose a random cell and add it to stack. After it we choose a random direction where unvisited cell is present and put that in stack. Keep repeating it till no more possibility is left. After this remove the cell from the stack and backtrack until you find a cell with unvisited neighbors. Repeat this process until the stack is empty and in end make a random exit point to finish maze creation.

**Solving Maze:**
There are many technique to solve maze like following left walls. Hear we will again will use the concept of stack and heap. The priority we will take is to first looks North, then East, then South and finally West. To solve maze, we will visit non visited neighbor cells (using stack to keep track), if there is multiple path then we will follow priority order. If we reach a deadend, then we will keep poping stack until we reach the previous multiple path, from where we will visit direction which is next in priority order. IF we had visited all patch then repeat this for the previous multiple path cell until we reach the exit point

**Showing the Solution:**
It is easy part as the sol from solving maze is stored, so we just have to display part by blinking different colour LED light 
![solution](https://user-images.githubusercontent.com/85681011/121859375-4163d100-cd15-11eb-91f3-c1eb3de73d3d.gif)




