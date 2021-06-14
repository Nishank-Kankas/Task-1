# MiniTask_2 of Task 1

## 1: Automatic Dog Feeder

**Problem Statement**: To make a device which will give food to dog at given time.

**Ideation and Planning**:

a) After selecting container, the first part is to bring food outside - using Servos for this.

b) monitoring food left is next part: using push button which work accourding to weight of container

c) informing the above info to owner: using LED light

d) to control all these, we need a microcontroller: using particle photon 

Part of the pipeline | Feasibility | Advantages | Disdvantages
------------ | ------------- | ------------- | -------------
Servo | Easy to use |  A very common device hence familiar to use | somewhat higher cost
Push button | easy to implement | Very simplified idea | just tell is food low or not, dont more accurate idea
LED light | easy to implement | simple and cheap | if not in field of view, wont notify
Particle Photon | cheaper but not much widely used | cheaper and smaller then other micro-controller | not enough liberary compare to arduino 

**Improvement**:

a) use buzzer when food is low, will notify even when not in field of view of user

b) webpage notification, so that even if user is out of house, they can get notified

c) one more buzzer of different frequency when its time to give food, it will notify the pet


