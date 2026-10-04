## Introduction to systems and Controls

**System**: An interconnection of subsystems to achieve some purpsoe (output or response) based on some input (refereence or desired response).

**Controls**: The process by which you design a driving signal (compensator or controller) to achieve the desired response.
 $$ R_s \to \text{Control System} \to C_{s}$$
 $Gain=\frac{C_{s}}{R_{s}}=\text{Transfer Function}$
 ![[Pasted image 20260901153823.png|490]]

Two ways to configure a system:
- Open Loop System: Output depends only on the $R_s \to Control System \to \text{Process Plant }G_{s} \to C_{s}$ which is low cost, does not handle disturbance
	- ![[Pasted image 20260901153958.png|449]]
- Closed Loop System: Forward Path, more complexity, handles disturbance. $F(s)=H(s) \cdot C(s)$ $E(s)=\text{Actuating Signal}=R(s)-F(s)$
	- 



![[Pasted image 20260901154729.png|376]]



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
	1. Cruise Control
	2. HVAC thermostats
	3. Robotic Arm
2. Functionaly, how do closed-loop systems differ from open-loop systems?
	1. Closed-loop measure the actual system ouput, feed it back to compare against the input reference, and continously adjust the control action based on calculated error
	2. Open-loop operate strictly based on input commands or fieed timing schedules without measuring or using the output to correct errors or disturbances.
3. State one condition under which the error signal of a feedback control system would not be the difference between the input and the output.
	1. When the feedback path contains a feedback element or transducer with a non-unity gain $H(s)\neq{1}$, scaling, or dynamic filtering
4. If the error signal is not the difference between input and output, by what general name can we describe the error signal?
	1. Actuating signal
5. Name the three major performance criteria for control systems
	1. Transient response
	2. Steady state error
	3. stability
6. Name the two parts of a system's total response
	1. Transient resoonse
	2. Steady State Response
7. What happens to the transient response for a stable system?
	1. it approaches zero as time approaches infinity
8. Describe a typical control system analysis task.
	1. Determing the dynamic behavior, stability, steady state accuracy, or transient performance of a given, fully specified control system configuration
9. Describe a typical control system design task.
	1. Specifiying, adjusting, or synthesis of system parameters and controllers to force an existing hardware system to satisfy a required set of performance specs
10. Adjustments to the forward path gain can affect the transient response. True or False?
	1. True, it changes the closed loop pole locations, altering properties such as damping ratio, natural frequency, and settling time.
11. Name three approaches to the mathematical modeling of control systems.
	1. Transfer Function
	2. State Space
	3. Differential Equation


What are the Design Stems of a control System?
1. Determine a physical system and specifications from requirements
2. Draw a functional block diagram
3. Represent the physical system as a schematic
4. Use the schematic to obtain a mathematical models of the system/subsystems.
5. Reduce the block diagram
6. Analyze and designe the system to meet requirements and specs. Including stability, transient response, and steady state performance
