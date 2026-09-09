---
title: "Industrial Automation Assembly Line"
excerpt: "Programming and integrating a Siemens PLC and Mitsubishi industrial robot as part of a multi-station automated production line"
categories:
  - Mechatronics & Automation
header:
  image: /assets/img/Auto1.jpeg
  teaser: /assets/img/Auto1.jpeg
---

**Role:** Mechanical Engineering Student, Group 4  
**Focus:** Industrial Automation, PLC Programming & Robotics  

---

<video width="100%" autoplay muted loop playsinline>
  <source src="/assets/img/Auto11.mp4" type="video/mp4">
</video>

---

## Project Overview

The goal of this project was to learn the fundamentals of **industrial automation and PLC programming** by programming one station of a small automated production line.

Our team's station was responsible for assembling a three-piece cell consisting of a **base, spring, and top**. To accomplish this, we learned to program and operate a **Mitsubishi industrial robot**, program a **Siemens S7-1500 PLC**, integrate sensors and pneumatic actuators, and communicate between our station and the other stations in the production line.

The project progressed from controlling individual pieces of equipment to successfully integrating our station into a **multi-station automated manufacturing process**.

---

## Learning Industrial Robotics

The first stage of the project focused on learning how to operate and program the **Mitsubishi industrial robot**.

Our station was responsible for the complete mechanical assembly of each cell. I helped program the robot to:

1. Pick up the incoming base of the cell.
2. Determine and correct the orientation of the base.
3. Place the base into the assembly fixture.
4. Pick up a spring and place it inside the base.
5. Pick up the top of the cell.
6. Determine and correct the orientation of the top.
7. Place the top onto the base and rotate it to secure the assembly.
8. Pick up the completed cell.
9. Deliver the finished assembly to the next station in the production line.

The robot was programmed using **MELFA-BASIC IV**, with taught positions defining the major pickup, alignment, assembly, and drop-off locations.

---

## Part Alignment & Sensor Feedback

One of the most interesting challenges was that the base and top could not simply be picked up and placed directly into the assembly. Their orientation first had to be determined.

To solve this, we used **sensor feedback combined with robot motion**.

For the base, the robot moved the part to an orientation-detection position and incrementally rotated it while monitoring a sensor. Once the sensor detected the required feature on the part, the robot stored that orientation and used it to correctly position the base in the assembly fixture.

We implemented a similar process for the top. The robot picked up the top, moved it to the sensing position, determined its orientation, and then used that information to correctly position and rotate the top onto the base.

This introduced us to using **sensor feedback within robot programming** rather than relying entirely on predetermined robot positions.

---

## Programming the Siemens PLC

After establishing the robot sequence, the next stage was learning how to control our station using a **Siemens S7-1500 PLC**.

We programmed the PLC logic for our station to determine when all of the required conditions were satisfied before allowing the robot to begin an assembly cycle.

Before starting the robot, the PLC needed to determine:

- Is a spring available?
- Is a top available?
- Are the component feeders in the correct position?
- Does a spring or top need to be dispensed?
- Has a new base arrived from the previous station?
- Is our station ready to begin another assembly cycle?

The PLC monitored sensors throughout the station and controlled pneumatic pushers that dispensed the spring and top when necessary.

This allowed the station to automatically prepare itself for the next assembly instead of requiring each component to be manually positioned.

---

## Sequence & Ladder Logic

A major focus of the project was learning how to translate the desired behavior of the machine into **PLC control logic**.

The sequence needed to coordinate sensors, pneumatic actuators, component availability, and the robot while preventing the station from progressing when the required conditions were not satisfied.

For example, if a spring was not already in position, the PLC would command the spring feeder to dispense one and then verify its presence using a sensor. The same process was used to prepare the top.

If the station determined that the feeder was completely out of components, the sequence instead entered an **error state** and waited for the operator to manually restock the station before continuing.

Once the spring, top, and incoming base were all ready, the PLC gave the robot permission to begin its assembly sequence.

---

## PLC-to-Robot Communication

Another important part of the project was learning how the PLC and industrial robot communicate.

The Siemens PLC and Mitsubishi robot controller exchanged signals through **digital I/O**. The PLC controlled signals used to enable the robot and start its programmed sequence, while the robot returned a completion signal once assembly was finished.

This created a handshake between the two systems:

**PLC verifies station → Robot receives permission → Robot assembles cell → Robot signals completion → PLC prepares next cycle**

The PLC therefore controlled *when* an assembly could occur, while the robot program controlled *how* the physical assembly was performed.

---

## Integrating with the Production Line

Once our individual station was functioning, the final challenge was integrating it with the stations programmed by the other teams.

We introduced **common variables shared between the teams** so that each station could communicate its current condition to the rest of the production line.

Two of the most important conditions were whether our station was:

- **Ready to receive another cell**
- **Experiencing an error**

This communication was important because our station could not operate independently from the rest of the line.

For example, if our spring feeder became empty, our PLC would identify the missing component and place our station into an error condition. The upstream station then needed to know **not to send another base** until our spring supply had been manually restocked and the error cleared.

This prevented parts from accumulating between stations and allowed the entire production line to respond to the condition of each individual workstation.

---

## Fault Handling & HMI

Our PLC logic also communicated with an **HMI** to provide information about the state of the station.

If the system detected that the spring or top feeder was empty, the PLC generated the corresponding fault condition and displayed it to the operator.

After manually restocking the missing components, the operator could acknowledge the condition through the HMI and allow the PLC sequence to resume.

This gave us experience with an important part of industrial automation: programming not only the normal operating sequence, but also determining **how the machine should respond when something goes wrong**.

---

## Full Assembly Sequence

By the end of the project, our station could automatically:

**Receive Base → Verify Components → Dispense Spring/Top if Needed → Enable Robot → Align Base → Place Base → Insert Spring → Align Top → Install & Twist Top → Transfer Completed Cell → Signal Completion**

The station then returned to its initial state and prepared for the next incoming cell.

---

## Final Integration

The final milestone was combining our station with the stations programmed by the other groups.

After integrating the shared PLC variables and coordinating the communication between stations, we successfully operated our section as part of the **complete automated production line**.

Rather than demonstrating only a single assembly cycle, the integrated line successfully produced **multiple completed cells consecutively**, with each team's station communicating with the others as the products moved through the manufacturing process.

---

## Reflection

This project gave me my first hands-on experience programming and integrating the types of controls used in **industrial automated equipment**.

The biggest takeaway was understanding that programming an individual robot or PLC is only one part of automation. The real challenge is getting **robots, PLCs, sensors, pneumatic actuators, HMIs, and neighboring machines to communicate and behave as one system**.

Working from the individual robot sequence through PLC programming and finally full production-line integration gave me practical experience with **Siemens PLC programming, ladder logic, Mitsubishi industrial robotics, MELFA-BASIC IV, sensor integration, pneumatic control, HMI fault handling, digital I/O, inter-station communication, and automated sequence control**.

---

{% include gallery caption="Industrial Automation Assembly Line Project Gallery" %}

