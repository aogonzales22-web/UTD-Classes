## Introduction to systems and Controls

**System**: An interconnection of subsystems to achieve some purpsoe (output or response) based on some input (refereence or desired response).

**Controls**: The process by which you design a driving signal (compensator or controller) to achieve the desired response.
 $$ R_s \to Control System \to C_{s}$$
 $Gain=\frac{C_{s}}{R_{s}}=\text{Transfer Function}$
Two ways to configure a system:
- Open Loop System: Output depends only on the $R_s \to Control System \to \text{Process Plant }G_{s} \to C_{s}$ which is low cost, does not handle disturbance
- Closed Loop System: Forward Path, more complexity, handles disturbance. $F(s)=H(s) \cdot C(s)$ $E(s)=\text{Actuating Signal}=R(s)-F(s)$

[

![Closed Loop Control - an overview | ScienceDirect Topics|249](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRPkhDbG4YdTyURHnleUWyqfTUlYQWrdsyigKIFNQxsIw&s=10)





]
- [x] %(https://www.google.com/imgres?q=Closed%20loop%20path%20systems%20and%20controls&imgurl=https%3A%2F%2Fars.els-cdn.com%2Fcontent%2Fimage%2F3-s2.0-B9780750646376500137-f13-61-9780750646376.gif&imgrefurl=https%3A%2F%2Fwww.sciencedirect.com%2Ftopics%2Fengineering%2Fclosed-loop-control&docid=7fUblz_heZCxEM&tbnid=kpFAeJoZWoATcM&vet=12ahUKEwjH5-GCo7yWAxVml2oFHbhBMOMQnPAOegQIfRAA..i&w=335&h=302&hcb=2&ved=2ahUKEwjH5-GCo7yWAxVml2oFHbhBMOMQnPAOegQIfRAA)%

## System  Representations
#### Dynamic System
A dynamic System is described by an $n^{th}$ order differential equation
	- N First order differential equation and put it in matrix form: state_space representation
	- use Laplace transform --> complex function Transfer Function(frequency domain)
$\text{Total Response}=\text{Transient Response}+\text{Steady State Respnse}$
Performance Criteria:
- Stability: Transient response must decay to zero as $t\to \infty$ or oscillates within some bounds
- System spec (transient response analysis)
- System accuracy (steady state response analysis)
- Cost
- Robustness (Low sensitivity to changes in system parameters)

Design Process:
- Specifications from the requirments
- Functional block diagram
- Modeling of subsystems
- Reduction of the system block diagram
- Analysis and design using test signals

Test Signals:
- Impulse Function
- Step Function
- Ramp Function
- Parabola Function 
- Sine/Cosine Functions


## Review Questions
1. Name three applications for feedback control systems.
2. Functionaly, how do closed-loop systems differ from open-loop systems?
3. State one condition under which the error signal of a feedback control system would not be the difference between the input and the output.
4. If the error signal is not the difference between input and output, by what general name can we describe the error signal?
5. Name the three major performance criteria for control systems
6. Name the two parts of a system's total response
7. What happens to the transient response for a stable system?
8. Describe a typical control system analysis task.
9. Describe a typical control system design task.
10. Adjustments to the forward path gain can affect the transient response. True or False?
11. Name three approaches to the mathematical modeling of control systems.


What are the Design Stems of a control System?
1. Determine a physical system and specifications from requirements
2. Draw a functional block diagram
3. Represent the physical system as a schematic
4. Use the schematic to obtain a mathematical models of the system/subsystems.
5. Reduce the block diagram
6. Analyze and designe the system to meet requirements and specs. Including stability, transient response