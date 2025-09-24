---
title: "VRT Outfeed Conveyor Optimization"
excerpt: "Doubling throughput capacity of Conagra’s VRT outfeed system"
header:
  image: /assets/img/VRT3.jpeg
  teaser: /assets/img/VRT3.jpeg
gallery:
  - url: /assets/img/VRT1.jpeg
    image_path: /assets/img/VRT1.jpeg
    alt: "Position 1 and 2 Pros and Cons"
    title: "Position 1 and 2 Pros and Cons"
  - url: /assets/img/VRT2.jpeg
    image_path: /assets/img/VRT2.jpeg
    alt: "Clearance, Staircase, and Bad Scan Conveyor"
    title: "Clearance, Staircase, and Bad Scan Conveyor"
  - url: /assets/img/VRT3.jpeg
    image_path: /assets/img/VRT3.jpeg
    alt: "Final Result"
    title: "Final Result"
  - url: /assets/img/VRT4.jpeg
    image_path: /assets/img/VRT4.jpeg
    alt: "Side View"
    title: "Side View"
  - url: /assets/img/VRT5.jpeg
    image_path: /assets/img/VRT5.jpeg
    alt: "Conveyor System"
    title: "Conveyor System"
---

**Role:** Project Engineering Intern, Conagra Brands  
**Timeline:** Summer 2025  
---

## Problem Statement  
At Conagra, the VRT outfeed system could not keep up with the rate of cases coming from the Combo 1 and Combo 2 production lines. Operators were forced to **hot stack cases** before they went into the freezer, and even then, the VRT could not outfeed at the same rate it was being infed.  

This mismatch caused the outfeed system to **back up and shut down the VRT**, which is directly connected to both production lines. Every time the freezer stopped, both production lines stopped, leading to significant downtime costs.  

---

## Goal  
My goal for this project was to **increase the throughput capabilities of the Variable Retention Freezer (VRT) outfeed system**. The system needed to handle the high case volume produced by two production lines, eliminate downtime caused by bottlenecks, and fit within the **existing space constraints** of the plant. The design also had to be financially viable, safe for operators, and fully integrated with the current palletizing system.  


---

## System Analysis  
The existing outfeed system included **four conveyor belt lines merging into a single DARP sorter**, which then sorted cases into four infeed lanes for palletizing robots.  

- The DARP sorter could only run at **67 cases/min**, and even at that speed, cases were falling on the floor and jams were frequent.  
- The DARP sorter became the bottleneck for the entire system, creating inefficiencies and limiting throughput.  

---

## Design Development  
To solve this, I proposed adding a **second DARP sorter**. Instead of four conveyor belts merging into one sorter, the design split the lines into two groups, each feeding into its own sorter. This effectively **doubled throughput capacity**, making the new bottleneck the palletizing robots and the freezer itself — leaving room for growth if either of those systems are improved later.  

### Space Constraint Challenge  
One of the biggest constraints was **fitting the second DARP sorter into the available space**. The existing area had an overhead platform for operator access, and since DARP sorters are uniquely thick, I had to carefully design around these limitations.  

I developed two possible solutions:  
1. **Install the new DARP sorter beneath the original sorter**  
2. **Install the new DARP sorter above the original sorter**  

![Position 1 and 2 Pros and Cons](/assets/img/VRT1.jpeg)

After leading a project team meeting, we decided to move forward with **Option 1**. This allowed operators to access cases from the ground with less steep inclines and declines, though it did restrict access to the middle of the palletizing robot infeed lanes.  

---

## Final Design Features  
Once the solution was chosen, I fleshed out the design in **Fusion 360** and added new components to make the system fully functional:  

- **New Bad Scan Lane** – Because DARP sorters rely on scanning cases to assign SKUs, I designed a new bad scan conveyor for the second sorter. This lane directed unreadable cases beneath and beside the original bad scan lane, consolidating them into one area for operator inspection.  
- **Operator Access** – Since the chosen solution blocked part of the operator pathway, I designed a new staircase connected to the overhead platform. This gave operators safe access to the middle of the palletizing robot infeed lanes.  
- **Clearances and Interference Checks** – Using Fusion 360, I verified clearances between cases, conveyors, and the overhead platform to ensure smooth operation with no interference.  

---
## CAD Model 
<iframe src="https://vanderbilt1079.autodesk360.com/shares/public/SH286ddQT78850c0d8a4e0001d78bd30e053?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

---

## Results  
- The final design **doubled the throughput capacity** of the VRT outfeed system.  
- The **new bottleneck** shifted to the palletizing robots and freezer itself, meaning the system is future-proof for higher capacities.  
- Achieved a **1-year ROI**, making the project highly cost-effective.  

This project gave me hands-on experience in balancing **process flow optimization, space constraints, operator safety, and ROI**, while showing me the value of clear communication between engineering and operations teams.

---
{% include gallery caption="VRT Outfeed Optimization Project Gallery" %}
