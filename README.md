# General Description: 
This repository tracks the contributions I've made towards building the vehicle that will represent UCLA Bruin Racing and compete in the annual Eco-Shell Marathon. Primarily, my contributions are towards the Powertrain sub-system team.

# PCB Design
The PCB was designed with the following in mind:
- Reducing distance between traces to minimize dissipation of power as well as improving efficiency since the actual connections are not entirely ideal. To reiterate, resistivity is proportional to length/distance of the resistive material. 
-For specific connections, the power loop between the mosfets and input capacitor should be as small as possible to minimize noise and parasitic induction. The SW trace connecting the inductor and the  mosfets should be as short and wide as possible to allow for maximum heat dissipation for the mosfets.
- The SW trace or the connections between the mosfets, inductor, and LM3150 chip or any other sources of noise should be placed away from the feedback loop. The feedback loop to the bottom left of the chip.
- Components that consume small amounts of current and power should be grounded to signal ground (the 5th pin from the top to the left) while components that need to consume a larger amount of power should be grounded to power ground. Components that require more power generate more heat and noise hence the need for a large copper plate to serve as ground to dissipate all of it. If the low-consumption components were connected to the same ground as the mosfets, the power ground signal could potentially contaminate the signal running through the low-consumption components hence why power ground and signal ground separated at the chip.
Some challenges included:
