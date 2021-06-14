## **1: Raspberry Pi Automated Plant Watering with Website**

**source**: https://www.hackster.io/ben-eagan/raspberry-pi-automated-plant-watering-with-website-8af2dc

**Aim**: To read mositure lvl of soil and water it when needed

**Material**:
Raspberry Pi, Relay, 3-6v Submersible Pump, Flexible Water Line, SparkFun Soil Moisture Sensor (with Screw Terminals)

**Details**: 
As the title and aim suggest, we want to set up Raspberry Pi so it can take reading of moisture and run pump when mositure lvl is low. we will first put the moisture senser in plant soil and connect the sensor with Raspberry Pi as shown in figure. All other part is also connected as in figure.

![image](https://user-images.githubusercontent.com/85681011/121859773-c0590980-cd15-11eb-97a7-9f5183928505.png)

**working**:
Resistance is inversely proportional to the soil moisture: so when moisture decrease, resistance will increase. Raspberry pi will take this value as input and when it exceddes a certain value (which tell water moisture is less), Pi will pass high voltage to relay which will result the circuit of power source and pump to complete. Hence pump will start and will supply water to plant till resistance decrease in moisture sensor. To see details, things are also displayed on a webpage.

code: [water.py](https://gist.github.com/benrules2/6f490f3a0e082ae6592a630bd7abe588), [web_plants.py](https://gist.github.com/benrules2/c4f3db455f4f2dfbe7d5b825b0b4ee36), [main.html](https://gist.github.com/benrules2/e43c469b2c1263237dc67010fca18b53)

**improvement**: Add a buzzer which start ringing if moisture level dont increase after 1-2min to notify us there is some problem in water source


## **2: Automatic Dog Feeder**
**Source**: https://www.hackster.io/Casey_Jacobson/automatic-dog-feeder-c890f6#toc-how-it-works-1

**Aim**: To make a device which will give food to dog accourding to time set by owner

**Material**: Particle Photon, Servos, LED, Pushbutton, Resistor of 10k and 1k

**Details**:

![image](https://user-images.githubusercontent.com/85681011/121868010-22b60800-cd1e-11eb-8b49-f921ef975e81.png)

The device is capable to give food to dog at given time as well as tell us when we need to refill the food. Giving food part is made by simply using Servo which will connected with photon. Servo role is to open the door for two second (we can change time if we want to give more/less food) during food time. 

To know about how much food is left, we are using a push sensor below food container. When there is food, it will be on due to weight otherwise off. We then connect the push button with a resistor to photon. We also connected red and green LED with it: green for 'food is there' and red for 'need refil'. 

code: [dogfeederbutton.md](https://github.com/Nishank-Kankas/Task-1/files/6647295/dogfeederbutton.md)

servo code: [dogfeederservo.md](https://github.com/Nishank-Kankas/Task-1/files/6647284/dogfeederservo.md)



## **3: Creating and Solving Mazes on a 128 x 64 LED Panel**

**Source**: https://www.hackster.io/doug-domke/creating-and-solving-mazes-on-a-128-x-64-led-panel-bb7740

**Aim**: Generate a random maze and then solve it

**Material**: Arduino Due, 64 by 32 LED panel, 5 volt 20 amp Power Supply, jumper wires

**Details:**
This is a coding focus project where we want to create a random maze with a unique solution - have unique random point of escape, on LED display amd then solve it. To create maze we implement regressive backtracking algorithm which mainly use the concept of stack and heap. 

To create maze, we will create an empty stack of list of cells. Then we will choose a random cell and add it to stack. After it we choose a random direction where unvisited cell is present and put that in stack. Keep repeating it till no more possibility is left. After this remove the cell from the stack and backtrack until you find a cell with unvisited neighbors. Repeat this process until the stack is empty and in end make a random exit point to finish maze creation.

![create_maze](https://user-images.githubusercontent.com/85681011/121861959-fa2b0f80-cd17-11eb-9681-acfdd4112bbb.gif)

Next part is solving the maze which we just created, There are many technique to solve maze like following left walls. Hear we will again will use the concept of stack and heap. The priority we will take is to first looks North, then East, then South and finally West. To solve maze, we will visit non visited neighbor cells (using stack to keep track), if there is multiple path then we will follow priority order. If we reach a deadend, then we will keep poping stack until we reach the previous multiple path, from where we will visit direction which is next in priority order. IF we had visited all patch then repeat this for the previous multiple path cell until we reach the exit point

![running](https://user-images.githubusercontent.com/85681011/121870153-5eea6800-cd20-11eb-929d-d93a50684382.gif)


Finally lets display solution. It is easy part as the sol from solving maze is stored, so we just have to display part by blinking different colour LED light 

![final_sol](https://user-images.githubusercontent.com/85681011/121862404-673ea500-cd18-11eb-9971-ab0c74e2a936.gif)

code: [Code.zip](https://github.com/Nishank-Kankas/Task-1/files/6647402/Code.zip)


## **4: Automatic fan control system using LM35 temperature sensor**

**Source**: https://www.hackster.io/Manishkr/automatic-fan-control-system-using-lm35-temperature-sensor-edbd80

**Aim**: To make a fun control system which work accourdingly to temp

**Material**: Arduino UNO, LM35, LED, Geared DC Motor - 12 V, Jumper wires, 9V battery

**Details**:
This project is to make an automatic fan which work when the room is hot. We had connected the system as shown in photo. Hear LM35 will tell us temp, if its more then 30degree then aurdino will run moter and turn green light on, otherwise red light will be on & moter off. 

![image](https://user-images.githubusercontent.com/85681011/121876564-40d43600-cd27-11eb-9ea3-509b4448387a.png)

Code: [Automatic fan control.zip](https://github.com/Nishank-Kankas/Task-1/files/6647521/Automatic.fan.control.zip)

Improvement: a small LED screen to display temperature, and a on-off button to controll manually

