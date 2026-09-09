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
  <source src="/assets/img/Auto12.mp4" type="video/mp4">
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

{% include gallery caption="Industrial Automation Assembly Line Project Gallery" %}

---
## Appendix

### PLC Variable Table

The Siemens PLC variables used to control the assembly station are shown below. The table is divided into two sections to make the complete I/O and HMI mapping easier to view at once.

<style>
.plc-table-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 25px;

  /* Makes the two tables wider, matching the robot appendix */
  width: 200%;
  margin-left: -50%;

  margin-top: 20px;
  margin-bottom: 40px;
  align-items: start;
}

.plc-table-column {
  min-width: 0;
}

.plc-table-column h4 {
  text-align: center;
  margin-top: 0;
  margin-bottom: 10px;
}

.plc-table-column table {
  width: 100%;
  font-size: 0.72em;
  line-height: 1.3;
  table-layout: auto;
}

.plc-table-column th,
.plc-table-column td {
  padding: 6px 7px;
  vertical-align: top;
}

.plc-table-column th {
  white-space: nowrap;
}

@media (max-width: 900px) {
  .plc-table-grid {
    grid-template-columns: 1fr;
    width: 100%;
    margin-left: 0;
  }

  .plc-table-column table {
    font-size: 0.8em;
  }
}
</style>


<div class="plc-table-grid">


<!-- ========================================================= -->
<!-- PLC TABLE COLUMN 1 -->
<!-- ========================================================= -->

<div class="plc-table-column">

<h4>Physical I/O</h4>

<table>
<thead>
<tr>
<th>Signal / Tag</th>
<th>Data Type</th>
<th>Address</th>
<th>I/O Category</th>
<th>Description / Function</th>
</tr>
</thead>

<tbody>

<tr>
<td><strong>R5</strong></td>
<td>Bool</td>
<td>%I1.5</td>
<td>Digital Input</td>
<td>Robot arm cycle finished signal</td>
</tr>

<tr>
<td><strong>I4</strong></td>
<td>Bool</td>
<td>%I0.4</td>
<td>Digital Input</td>
<td>Spring presence sensor</td>
</tr>

<tr>
<td><strong>I5</strong></td>
<td>Bool</td>
<td>%I0.5</td>
<td>Digital Input</td>
<td>Top presence sensor A</td>
</tr>

<tr>
<td><strong>I6</strong></td>
<td>Bool</td>
<td>%I0.6</td>
<td>Digital Input</td>
<td>Top presence sensor B</td>
</tr>

<tr>
<td><strong>I0</strong></td>
<td>Bool</td>
<td>%I0.0</td>
<td>Digital Input</td>
<td>Feed / position sensor 0</td>
</tr>

<tr>
<td><strong>I1</strong></td>
<td>Bool</td>
<td>%I0.1</td>
<td>Digital Input</td>
<td>Feed / position sensor 1</td>
</tr>

<tr>
<td><strong>I2</strong></td>
<td>Bool</td>
<td>%I0.2</td>
<td>Digital Input</td>
<td>Feed / position sensor 2</td>
</tr>

<tr>
<td><strong>I3</strong></td>
<td>Bool</td>
<td>%I0.3</td>
<td>Digital Input</td>
<td>Feed / position sensor 3</td>
</tr>

<tr>
<td><strong>O0</strong></td>
<td>Bool</td>
<td>%Q0.0</td>
<td>Digital Output</td>
<td>Actuator / spring pusher</td>
</tr>

<tr>
<td><strong>O1</strong></td>
<td>Bool</td>
<td>%Q0.1</td>
<td>Digital Output</td>
<td>Actuator / top pusher</td>
</tr>

<tr>
<td><strong>O1.1</strong></td>
<td>Bool</td>
<td>%Q1.1</td>
<td>Digital Output</td>
<td>Turns on operation rights</td>
</tr>

<tr>
<td><strong>O1.2</strong></td>
<td>Bool</td>
<td>%Q1.2</td>
<td>Digital Output</td>
<td>Starts the robot servos</td>
</tr>

<tr>
<td><strong>OR</strong></td>
<td>Bool</td>
<td>%Q0.2</td>
<td>Digital Output</td>
<td>Starts the robot program</td>
</tr>

<tr>
<td><strong>O1.0</strong></td>
<td>Bool</td>
<td>%Q1.0</td>
<td>Digital Output</td>
<td>Turns off the robot servos</td>
</tr>

</tbody>
</table>

</div>



<!-- ========================================================= -->
<!-- PLC TABLE COLUMN 2 -->
<!-- ========================================================= -->

<div class="plc-table-column">

<h4>PLC Memory & HMI Variables</h4>

<table>
<thead>
<tr>
<th>Signal / Tag</th>
<th>Data Type</th>
<th>Address</th>
<th>I/O Category</th>
<th>Description / Function</th>
</tr>
</thead>

<tbody>

<tr>
<td><strong>Spring Missing</strong></td>
<td>Bool</td>
<td>%M100.0</td>
<td>Memory Bit / HMI Status</td>
<td>Diagnostic error flag sent to the HMI when springs are unavailable</td>
</tr>

<tr>
<td><strong>Top Missing</strong></td>
<td>Bool</td>
<td>%M100.1</td>
<td>Memory Bit / HMI Status</td>
<td>Diagnostic error flag sent to the HMI when top caps are unavailable</td>
</tr>

<tr>
<td><strong>Ready</strong></td>
<td>Bool</td>
<td>%M1.0</td>
<td>Memory Bit / HMI Status</td>
<td>System ready status displayed on the HMI and used for line communication</td>
</tr>

<tr>
<td><strong>Finished Piece</strong></td>
<td>Bool</td>
<td>%M100.2</td>
<td>Memory Bit / HMI Status</td>
<td>Cycle complete / finished piece indicator</td>
</tr>

<tr>
<td><strong>Springs Restocked</strong></td>
<td>Bool</td>
<td>%M100.3</td>
<td>Memory Bit / HMI Input</td>
<td>Fault reset pulse from the HMI after springs have been restocked</td>
</tr>

<tr>
<td><strong>Tops Restocked</strong></td>
<td>Bool</td>
<td>%M100.4</td>
<td>Memory Bit / HMI Input</td>
<td>Fault reset pulse from the HMI after tops have been restocked</td>
</tr>

</tbody>
</table>

</div>


</div>


---

### Mitsubishi MELFA-BASIC IV Robot Program

<style>
.robot-appendix-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 20px;
  width: 200%;
  margin-left: -50%;
  margin-top: 25px;
  align-items: start;
}

.robot-appendix-column {
  min-width: 0;
}

.robot-appendix-column h3 {
  margin-top: 0;
  margin-bottom: 12px;
  font-size: 1.05em;
  text-align: center;
}

.robot-appendix-column pre {
  margin: 8px 0 10px 0 !important;
  padding: 10px !important;
  font-size: 0.68em !important;
  line-height: 1.35 !important;
  white-space: pre-wrap !important;
  overflow-x: visible !important;
  word-break: normal !important;
  border-radius: 4px;
}

.robot-appendix-column code {
  white-space: pre-wrap !important;
  font-size: inherit !important;
}

.robot-code-note {
  font-size: 0.78em;
  line-height: 1.45;
  margin: 5px 2px 18px 2px;
}

@media (max-width: 900px) {
  .robot-appendix-grid {
    grid-template-columns: 1fr;
  }

  .robot-appendix-column pre {
    font-size: 0.78em !important;
  }

  .robot-code-note {
    font-size: 0.9em;
  }
}
</style>


<div class="robot-appendix-grid">


<!-- ========================================================= -->
<!-- COLUMN 1 -->
<!-- ========================================================= -->

<div class="robot-appendix-column">

<h3>1. Initialization & Base Alignment</h3>

<pre><code>10 DEF POS PAUX
20 DEF POS PAUX2
30 DEF IO PORT10 = BIT, 10
40 DEF IO PORT8 = BIT, 8
50 DEF IO PORT7 = BIT, 7
60 DEF IO FINISH = BIT, 5
70 DEF IO PORT6 = BIT, 6
80 OVRD 20</code></pre>

<p class="robot-code-note">
Lines 10–80 define the input/output ports and position variables used throughout the program. The robot operating speed is also set to 20%.
</p>


<pre><code>90 FINISH = 0
100 HOPEN 1
110 MOV P1

120
130 WHILE (PORT8 = 0)
140 DLY 1
150 WEND
160</code></pre>

<p class="robot-code-note">
The FINISH output is reset, the gripper is opened, and the robot moves to its idle position P1. The robot then waits until PORT8 detects that a base has arrived before beginning the assembly sequence.
</p>


<pre><code>170 WHILE (PORT8)
180 MOV P10, -10
190 MOV P10
200 HCLOSE 1
210 MOV P10, -10
220 MOV P1
230 MOV P20, -10
240 MOV P20
250 HOPEN 1
260 MOV P1
270 WEND</code></pre>

<p class="robot-code-note">
The robot approaches base pickup position P10 using a vertical offset to reduce the risk of collision, closes the gripper, and returns through the idle position. It then moves to P20 and releases the base. The WHILE loop allows the robot to repeat the pickup if PORT8 still detects the base, indicating that the first pickup was unsuccessful.
</p>


<pre><code>280 MOV P21, -10
290 MOV P21, 3
300 HCLOSE 1
310 MOV P21, -10</code></pre>

<p class="robot-code-note">
The robot returns to the base at P21 and picks it up using the center gripper position so that its orientation can be determined.
</p>


<pre><code>320 MOV P23
330 PAUX = P23
340 DLY 1</code></pre>

<p class="robot-code-note">
The base is moved to orientation-detection position P23. A one-second delay gives the sensor time to stabilize, and the current robot position is stored in the variable PAUX.
</p>


<pre><code>350 WHILE (PORT10)
360 PAUX.A = PAUX.A + 0.2
370 MOV PAUX
380 WEND

390 PAUX2 = P24
400 PAUX2.A = PAUX.A + 0.2
410 MOV PAUX2, -25
420 MOV PAUX2
430 HOPEN 1
440 MOV P1

450
460
470
480</code></pre>

<p class="robot-code-note">
While PORT10 remains active, the robot rotates the base in 0.2 radian increments. Once the sensor reaches the locating feature on the part, PORT10 changes state and the loop ends. The detected orientation is stored and transferred to PAUX2 with an additional 0.2 radian offset. The robot then places the correctly oriented base at P24 and returns to idle.
</p>

</div>



<!-- ========================================================= -->
<!-- COLUMN 2 -->
<!-- ========================================================= -->

<div class="robot-appendix-column">

<h3>2. Spring & Top Assembly</h3>

<pre><code>490 'SPRING

500 MOV P40, -10
510 MOV P40, 3
520 HCLOSE 1
530 MOV P40, -30
540 MOV P41, -30
550 MOV P41
560 HOPEN 1
570 MOV P41, -30
580 MOV P1

590
600
610
620
630</code></pre>

<p class="robot-code-note">
The robot picks up the spring at P40 and places it inside the base at P41. Larger vertical offsets are used during this sequence because the spring must be inserted down into the base rather than simply placed on top of it.
</p>


<pre><code>640 'TOP

650 WHILE (PORT6 = 0)
660 HOPEN 1
670 MOV P55
680 MOV P50, -10
690 MOV P50, 4
700 HCLOSE 1
710 MOV P50, -10
720 MOV P55
730 MOV P60, -30
740 MOV P60, -3
750 WEND

760
770
780
790
800</code></pre>

<p class="robot-code-note">
PORT6 is connected to the sensor used to verify that the top has been successfully removed from its pickup location. The robot approaches P50 through midpoint P55, closes the gripper, and moves toward the orientation-detection position. If the sensor indicates that the top was not successfully picked up, the robot repeats the sequence.
</p>


<pre><code>810 'PLACE TOP

820 PAUX = P60
830 DLY 1
840 ON PORT7 GOTO 90</code></pre>

<p class="robot-code-note">
The robot stores the top's current position in PAUX and pauses briefly to allow the orientation sensor to stabilize. PORT7 provides an additional condition that can return the robot to the beginning of the program if required.
</p>


<pre><code>850 WHILE (PORT10 = 0)
860 PAUX.A = PAUX.A - 0.1
870 MOV PAUX, -3
880 WEND</code></pre>

<p class="robot-code-note">
The robot incrementally rotates the top while monitoring PORT10. The top is rotated in 0.1 radian increments until the sensor detects the locating feature. The opposite rotation direction is used from the base-alignment operation to avoid reaching the robot's rotational limit.
</p>


<pre><code>890 PAUX2 = P24
900 PAUX2.A = PAUX.A - 0.1
910 MOV PAUX, -20
920 MOV PAUX2, -25
930 MOV PAUX2, 1
940 PAUX2.A = PAUX2.A + 1.9
950 MOV PAUX2, 1
960 HOPEN 1
970 MOV P1

980
990
1000</code></pre>

<p class="robot-code-note">
The detected top orientation is transferred to PAUX2 at the base assembly position P24. The robot moves the top into position and then rotates it approximately 1.9 radians to secure the top onto the base. Once the top has been installed, the gripper opens and the robot returns to its idle position.
</p>

</div>



<!-- ========================================================= -->
<!-- COLUMN 3 -->
<!-- ========================================================= -->

<div class="robot-appendix-column">

<h3>3. Finished Part & Cycle Reset</h3>

<pre><code>1010 'DROPOFF

1020 MOV P63, -20
1030 MOV P63
1040 HCLOSE 1

1050

1060 MOV P63, -20

1070

1080 MOV P1, -20
1090 MOV P64, -20
1100 MOV P64
1110 HOPEN 1
1120 MOV P64, -10
1130 MOV P1

1140
1150</code></pre>

<p class="robot-code-note">
The completed assembly is picked up at P63 using the back gripper and transferred to final drop-off position P64. The robot moves through an offset from the idle position because the final drop-off location is relatively high. This intermediate movement provides additional clearance and reduces the possibility of a collision.
</p>


<pre><code>1160 FINISH = 1
1170 DLY 1
1180 GOTO 90</code></pre>

<p class="robot-code-note">
Once the completed part has been delivered, FINISH is set to 1. This digital output tells the Siemens PLC that the robot has completed its assembly cycle so that the PLC can turn off the servos and signal that a finished part is available.
</p>

<p class="robot-code-note">
The one-second delay gives the PLC enough time to reliably read the FINISH signal. The program then returns to line 90, resets the completion signal, opens the gripper, returns to the idle position, and waits for the next base to arrive.
</p>


<h3>Program Sequence</h3>

<p class="robot-code-note">
The complete robot sequence can be summarized as:
</p>

<p class="robot-code-note">
<strong>
Detect Base → Pick Up Base → Determine Orientation → Position Base → Insert Spring → Pick Up Top → Determine Orientation → Install & Rotate Top → Pick Up Completed Assembly → Transfer to Next Station → Signal PLC → Reset
</strong>
</p>


<h3>Key Program Elements</h3>

<p class="robot-code-note">
<strong>PAUX / PAUX2:</strong> Temporary position variables used to modify and store detected component orientations.
</p>

<p class="robot-code-note">
<strong>PORT8:</strong> Detects the incoming base and confirms successful pickup.
</p>

<p class="robot-code-note">
<strong>PORT10:</strong> Provides feedback during base and top orientation detection.
</p>

<p class="robot-code-note">
<strong>PORT6:</strong> Verifies successful pickup of the top.
</p>

<p class="robot-code-note">
<strong>FINISH:</strong> Communicates completion of the robot cycle back to the Siemens PLC.
</p>

<p class="robot-code-note">
<strong>HOPEN / HCLOSE:</strong> Commands the pneumatic robot gripper to open and close.
</p>

<p class="robot-code-note">
<strong>MOV:</strong> Commands movement between taught robot positions and calculated position offsets.
</p>

</div>


</div>

