---
title: "Syringe Pump"
excerpt: "DIY syringe pump capable of 1 ul / min flow rate up to 10 mL / min"
header:
  image: /assets/img/Syringe 2.pdf
  teaser: /assets/img/Syringe 2.pdf
gallery:
  - image_path: /assets/img/Syringe 2.pdf
 
   
---

# Design

Gear-ate Syringe Pump
As a key member of a collaborative team, the Gear Gurus, I contributed to the design and fabrication of a functional syringe pump as part of our rapid prototyping course. Our project encompassed three main sectors: CAD, circuitry, and coding, emphasizing teamwork and communication. 

Design and Fabrication: 
Using Fusion 360, I designed custom components such as end supports, a motor mounting plate, and an enclosure, ensuring compatibility with both 10 mL and 20 mL syringes. These components were then sliced and 3D printed.

# CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH512d4QTec90decfa6e6924d2751dcf233c?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

# Markdown Table
Link to table of custom and off the shelf parts [Bill of Materials](https://vanderbilt643.autodesk360.com/g/projects/20220916557357901/data/dXJuOmFkc2sud2lwcHJvZDpmcy5mb2xkZXI6Y28uR1JZUUdBeHFRTzZtVDJEcFFDY05fUQ/dXJuOmFkc2sud2lwcHJvZDpkbS5saW5lYWdlOkVHRDY0ME9RVEYyMllrUUVnaFRXeUE/bom?compositionType=WORKING&version=75)

# Arduino Code

I developed and refined the Arduino code to allow for user-friendly input of syringe type and flow rate, translating these parameters into accurate stepper motor control for constant liquid delivery.

Link to Arduino [code](https://docs.google.com/document/d/14Vla2uPnEnLVWwXNtGN3LCafFqIqiaF9xacnmZB2fOg/edit?usp=sharing)

# Operating instructions

The syringe pump is a precision device designed to accurately deliver liquid from syringes, typically used in medical applications. To operate, first ensure the syringe is securely mounted by placing its barrel flange into the prongs of the end support and the tip resting on the syringe tip support. Manually retract the carriage before powering on the device. Once the device is connected to a 12V power source, input the desired flow rate (in mL/min) and syringe type (either 10 mL or 20 mL) into the Arduino code, then upload it. The device is controlled using a latching button on the front of the enclosure: pressing the button starts the syringe pump, and the green LED will light up to indicate the motor is running and the syringe plunger is dispensing fluid. Pressing the button again pauses the device, with the yellow LED indicating a pause while liquid remains in the syringe. To stop the pump entirely, press the button once more, and the red LED will light up, signaling the syringe is empty or the motor has stopped. The pump's operation is governed by the flow rate and syringe size, with the maximum flow rate being 60 mL/min for a 10 mL syringe and 107.3 mL/min for a 20 mL syringe. A limit switch provides feedback to stop the motor when the carriage reaches its endpoint, preventing the syringe from running dry. The system can be easily modified for different syringes by updating the flow rate and syringe size in the code. However, the syringe pump is designed for 10 mL and 20 mL syringes, and other sizes are not supported without modifications. After use, the device should be powered down and the syringe pump cleaned to maintain functionality.


{% include gallery caption="Large Format 3D Printer Gallery" %}
