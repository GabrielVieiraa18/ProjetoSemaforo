## Project traffic light crossing simulator
link github: https://github.com/GabrielVieiraa18/ProjetoSemaforo)

language: "wokwi"

wokwi_id: 375245713375900673

## How does it works?

This circuit will use the chips internal clock and the PCBs low-level reset. The project in question belongs to the domain of traffic control systems and involves the implementation of a simulation of a traffic light using logical gate circuits. The simulation scenario takes place at an intersection composed of two main avenues, offering drivers the option to proceed straight or make a turn in their respective directions. In this context, four sets of traffic lights are present, but the control logic is applied to only two of them simultaneously. The system also incorporates a state dedicated to pedestrians, activated when all vehicle traffic lights display the red color, thus allowing safe pedestrian crossing. The overall operation of the system is based on logical combinations that determine each of the possible states:

State 1: Traffic Light 1: Green - Traffic Light 2: Red - Pedestrian Traffic Light: Red;
State 2: Traffic Light 1: Yellow - Traffic Light 2: Red - Pedestrian Traffic Light: Red;
State 3: Traffic Light 1: Red - Traffic Light 2: Green - Pedestrian Traffic Light: Red;
State 4: Traffic Light 1: Red - Traffic Light 2: Yellow - Pedestrian Traffic Light: Red;
State 5: Traffic Light 1: Red - Traffic Light 2: Red - Pedestrian Traffic Light: Green.

The interaction between functional blocks is carried out through control logic, which depends on the conditions of vehicle traffic lights and pedestrian traffic lights. The sequence of states is determined by the combinations of signals applied to the traffic lights, aiming to optimize vehicle circulation and ensure pedestrian safety at the intersection.

To implement the operation of each state, counters based on D-type flip-flops were used, operating synchronously with the use of a multiplexer (mux). These counters were designed to represent the different states of the traffic lights, with each state being associated with a specific count. The adopted method involves the use of binary counters, which are sequentially activated to produce the desired sequence of states.

The counting process is carried out by configuring three interconnected flip-flops that perform binary counting. These flip-flops receive three inputs that determine their count according to the planned sequence of states. Additionally, an additional flip-flop is employed to create the necessary counting module. This flip-flop acts as a frequency divider, sending a high-level logic signal to the D command input, resulting in a restart of the counting when needed.

The proper combination and coordination of these flip-flops, along with the mux, allow the creation of control logic that generates the sequence of traffic light states according to the defined criteria. Synchronous synchronization of the flip-flops with the assistance of the mux ensures smooth transition between states, effectively simulating the operation of traffic lights at a real traffic intersection. This project incorporates principles of digital circuits and combinational logic to achieve a functional and coherent traffic light control system.

## How to test it?
For testing, it is possible to observe each state indicated by the traffic light. There is a reset button that resets the system. In general, there is hardware setup, initial states, input signals, output monitoring, pedestrian activation, and a cycle of states.

Hardware Setup: Configuring the physical components of the system.
Initial States: Defining the initial conditions of the system.
Input Signals: Simulating signals that represent various scenarios.
Output Monitoring: Observing the system's responses and outputs.
Pedestrian Activation: Ensuring pedestrian safety when required.
Cycle of States: Verifying the sequence of traffic light states.    

## Pictures:
<img src=diagrama.PNG>

## Inputs:

CLK

RESET


## Outputs:

S1 Red

S1 Yellow

S1 Green

S2 Red

S2 Yellow

S2 Green

Red Pedestrians

Green Pedestrians

## Resources

- [FAQ](https://tinytapeout.com/faq/)
- [Digital design lessons](https://tinytapeout.com/digital_design/)
- [Learn how semiconductors work](https://tinytapeout.com/siliwiz/)
- [Join the community](https://discord.gg/rPK2nSjxy8)
