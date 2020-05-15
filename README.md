# DELIVR Project
## Concept
<p align="center">
  <img src="Images/Prototype_DELIVR.png">
</p>
A delivery company uses drones to deliver small shipments from its business building to their customers. DELIVR is a training VR system for new staff. To better understand the customer experience, the drone operators must switch roles with the end-customers to experience the package delivery and improve it. Safety protocol practices are essential to this project. The drone operators must review and save their scores at the end of the experience. 

A manager will review the scores of the staff after completing the VR training course and will decide if the trainee is capable of operating the drones to real deliveries.

## Scope

### Functional Requirements

- The operator **receives** a new shipment order.
- Operator **starts** the drone program.
- Program has a short tutorial to **understand** the control of the drone.
- Operator **locates** the pickup destination.
- Controls must **simulate** actual drone movement and control.
- The simulation **highlight** the position of the package.
- Operator **picks up** package.
- Operator **locates** the drop off destination.
- The simulation **shows** current time and delivery time.
- The customer **recieves** a notification that the delivery is close.
- The customer **moves** towards a specific location to recieve the package.
- Operator **drops off** the package.
- The operator **confirms** delivery.
- Operator **returns** the drone to central office.

### User Experience

Once the operator enters the simulation in VR, she/he will be in a room similar to the one physically found in real life.  A computer where notifications, deliveries, and emails can be received is in front of the user. Within the work area there are different interactable objects with the objective of creating an immersive and entertaining environment.

The operator receives a notification about a new available delivery, accepts it and begins the flight simulation.

The drone is activated and the interface instructs the operator on how to take off and subsequently test the drone's movement, a process that will serve to train the operator and at the same time verify that the drone works properly.

Once the process aboved explained is complete, a mini map will be added in the interface to guide the operator to the pick up destination. The current time as well as the delivery time will be added to the interface for the operator to calculate the flight time.

One package can be delivered at once. The user is free to navigate wherever he/she wants but the fastest he/she gets to the delivery destination the better the score, which they can’t see until the simulation is over.  

When the operator gets close enough to the drop off location, the level changes so he can control the client that is waiting for the package for him to understand completely the process of delivery. The client should receive a notification saying the delivery is close and needs to approach to a pick up location without being so close, or the drone won’t drop the delivery.

Once the delivery is finished, the operator has to confirm it. If he/she does the confirmation before the client pick ups the package, the score will drop.

After confirmation the operator will return to the main office to recharge the drone and wait for the next job.

### Task

- Import and optimize the 3D models.

	- Street buildings, warehouse bay, residential house, drone Content Prep

	- Organize the Content browser. Content Prep

	- Review the 3D models before importing into UE. Content Prep

	- Optimize any high-poly mesh. Content Prep

2. Create a street block.

a. Create a new level. style

b. Add static mesh models to the level to recreate a street block. style

c. Add lighting for the street. style

3. Creating the contact site between the drone and the delivery.

a. Add collision to the drone for overlap events

b. Add a delivery pawn (receiver) to hand over the package. style

c. Import animation BP or overlap event to detect drone is approaching. Content Prep

d. Drone communicate with the delivery pawn through level BP, Dispatch, or state machine for the delivery animation BP.

4. Program the HUD for the pilot of the drone.

a. Study IFR references.

b. Calculate speed in BP. Function

c. Get score from GameMode or GameScore. Function

d. Count down for the delivery time. Function

e. Track the altitude and latitude (Yaw offset). Use a holo-drone to visually track drone orientation. Function

f. Add a google-map like cutout for navigation. Style

i. Develop BP for the mini map. Function

g. Add emergency button input. Content Prep

i. Develop BP for emergency button. Function

h. Add battery life graphic to the HUD. Content Prep

i. Developer BP for battery life. Function

i. Add package info to the HUD. Content Prep

i. Quantities, labels, weight, defects, etc.

ii. Develop BP to display package info for HUD Function

j. Add signal strength graphic to the HUD. Content Prep

i. Develop BP for low or high signal strength. Function

k. Add an auto-pilot input. Content Prep

i. Develop BP for the auto-pilot event. Function

l. Add pickup and drop-off input. Content Prep

i. Develop BP for auto pickup and drop-off events. Function

m. Add a re-calibrate input. Content Prep

i. Develop BP to auto-readjust the drone level Function

n. Add start and stop input. Content Prep

i. Develop BP for turn-on and off events. Function

5. Add motion controller inputs to the vr pawn. All the drone controls are on the sticks Function

a. Add rotation and movement for the controllers

b. Add haptics for collision

c. Add switch mode from ground to drone

d. Print tasks from enum

e. Add auto pilot event

f. Add right trigger for speed.

g. Add left trigger for slow to stop.

h. Add left thumbstick for direction control

i. Add right thumbstick for YAW rotation

j. Add grip to drop or pickup event

k. Add X for emergency stop to zero the speed or hovers to closest safehouse.

6. Add sensors to the drone Function

a. Radial trace or spherical trace.

7. Add feedback system: Function

a. Make an Enum list of tasks to complete.

b. Print the enum list for the player.

c. Add switch by Enum to go to next task.

d. Add a TimeNode to track time per task.

e. Add a help assist for when TimeNode finishes

8. Add thirdperson pack for UE. Content Prep

9. Add mannequin to the level. style

a. Add collision to detect drone approaching Function

b. Import animation for reacting to the drone approach Content Prep

c. Add task complete event to the mannequin actor. Function

10. Add a capture cam to the drone HUD for monitoring the delivery basket. style

11. Add different weather to the Game Mode. style

a. Add sunlight control to level BP. Function

b. Add city control to the level Bp. Function

12. Add save to game state for manager to review. Function

a. Add new level for managers. style

b. Add widget to print scores. style

c. Add game scores to the new level. Function

d. Add sound. style

e. Add widget interact to use oculus touch as a laser pointer Function

13. Add receiver experience

a. Bind the delivery pawn with drone dispatches. Function

b. Add input to switch from drone to the receiver. Content Prep

14. Create actor for the delivery package. Content Prep

a. Add grabbale interface Function

b. Add pickup and drop events Function

15. End the game when the player (the consumer) picks up the package.

a. Level BP fades camera to black. style
