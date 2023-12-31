# IDM Circular Road Startup Animation
First click the green code button in the upper right corner, then click the third DOWNLOAD ZIP to download and unzip it.Once downloaded, you can open it directly with your browser to see the circular road as well as the buttons (which are relatively small). Press play to see the vehicles move, the simulation is short. The direction of the arrow is the direction of the front of the vehicle.
 In the circular road simulation, we often set up a scene with a very high density to verify the latter part of the flow density graph. However, due to random distribution of vehicles, occasionally vehicles are set with initial spacing less than congestion spacing (which can also occur when the density is too high). 
 
Other Scenes

An essential point to note is that drivers cut in line when traffic is congested, resulting in distances smaller than the jam distance s0. In these situations, vehicles move slowly and stop-and-go traffic occurs frequently. We know that reversing in congested environments is dangerous and could lead to rear-end collisions of vehicles due to the smaller spacing between them. Reversing a vehicle in a simulation environment could also cause a crash of the simulation. In real-life and simulation scenarios, we can observe several primary situations:

i) At on- and off-ramps, when the main vehicle needs to force a lane change to enter the off-ramp exit or to enter the main roadway from the on-ramp, if the roadway in the vicinity of the on-ramp is congested, then the main vehicle needs to forcibly cut into the congested road. At this time, most of the vehicles near the ramp are stationary and maintain a jam distance s0 (due to heterogeneity between vehicles, each vehicle’s s0 is different). The main vehicle’s cutting behavior will cause the distance between the main vehicle and the vehicle being cut in line to be less than the s0 of the vehicle being cut in line. In real life, when facing cutting behavior in a congested environment, most drivers will choose to remain stationary and let the cutting vehicle enter the gap. But contrary to reality, IDM chooses to produce reverse acceleration from a stationary state, resulting in reversing. We know this is unsafe and in congested simulation environments, reversing behavior of cut-in vehicles often causes vehicles behind them to also reverse, resulting in chaotic traffic flow. Next, we give an example diagram of an off-ramp as shown in Fig. A, which demonstrates the simulated reversing problem for the above IDM.
![1](https://github.com/chanstary/IDM-Circular-Road-Startup-Animation/assets/83267051/1db29b8a-d30f-4f8e-8bf8-7e69b53116cf)
Fig. A1 Before the main vehicle cuts in line
![2](https://github.com/chanstary/IDM-Circular-Road-Startup-Animation/assets/83267051/1e8200b8-3c28-4c83-ad04-04407569604f)
Fig. A2 After the main vehicle cuts in line
Fig. A Following vehicle reversing at the off-ramp

ii) A similar situation also occurs when waiting for a traffic light at an intersection entrance. In real life, the main vehicle often fails to notice that it has taken the wrong lane due to distraction or unfamiliarity with the road. In this case, the main vehicle will choose to forcibly cut into the desired lane before the intersection, causing the above problem mentioned in (i). In simulations, when the main vehicle has not completed its lane selection path planning before queuing and the queue length before the intersection is too long, It may force a lane change to reach the desired lane. This situation can also cause vehicles queuing at intersections to reverse. The intersection entrance scenario is shown in Fig. B.
![3](https://github.com/chanstary/IDM-Circular-Road-Startup-Animation/assets/83267051/515b6a64-f03f-44da-a297-892857f86521)
Fig. B1 Before the main vehicle cuts in line
![4](https://github.com/chanstary/IDM-Circular-Road-Startup-Animation/assets/83267051/affe9925-7569-4636-8b15-c84b969e3065)
Fig. B2 After the main vehicle cuts in line
Fig. B Following vehicle reversing at intersection entrance
