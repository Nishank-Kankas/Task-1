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
LED light | easy to implement | simple and cheap | dont notify owner they are in other room
Particle Photon | cheaper but not much widely used | cheaper and smaller then other micro-controller | not enough liberary compare to arduino 

