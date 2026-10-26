---
title: "Drone-Delivered Exothermic Blood Warmer"
excerpt: "Using human-centered design to develop a lightweight, battery-free blood warmer for emergency drone delivery in Ukraine"
categories:
  - Design Engineering
  - Research and Experimental
header:
  image: /assets/img/Blood8.png
  teaser: /assets/img/Blood8.png
---

<style>
@media (min-width: 1024px) {
  .page {
    width: 100% !important;
    padding-right: 0 !important;
    float: none !important;
  }

  .page__inner-wrap {
    width: 100% !important;
  }

  .page__content {
    width: 100% !important;
  }
}

.blood-two-column {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 25px;
  align-items: center;
  margin: 20px 0;
}

.blood-two-column img {
  width: 100%;
  height: auto;
}

@media (max-width: 900px) {
  .blood-two-column {
    grid-template-columns: 1fr;
  }
}
</style>

**Role:** Mechanical Engineering Student, Interdisciplinary Design Team  
**Course:** How to Make Anything and Make It Matter  
**Focus:** Human-Centered Design, Rapid Prototyping & Experimental Testing  

---

## Project Overview

For our *How to Make Anything and Make It Matter* course, my team partnered with **Tim Bongartz** to investigate an emergency medicine challenge currently faced in Ukraine. Tim spent time with Ukrainian soldiers near the front lines and identified an opportunity to improve the emergency blood delivery process.

At the heart of our project was one urgent problem:

### **Injured Ukrainian Soldiers Need Warm Blood Fast in an Unprecedented Drone War Zone**

![Project Team](/assets/img/Blood1.png)

---

## Project Background

The war in Ukraine has created a battlefield unlike almost any that came before it in its dependence on small unmanned aircraft. Different units may use completely different drones, and those aircraft are regularly modified, jammed, damaged, or shot down.

Drones are not only used for reconnaissance and combat. They can also transport critical medical supplies into areas where sending a person or vehicle may be extremely dangerous.

One of those resources is **blood**.

At drone stations behind the front line, blood is kept refrigerated until an injured soldier requires an emergency transfusion. The existing delivery process is approximately:

**Remove Blood from Refrigeration → Warm Blood in a Water Bath → Package Blood → Load Drone → Fly to Front Line → Drop Blood to Soldiers**

The warming step alone can add roughly **10–12 minutes before the drone even leaves**, but warming is important because transfusing cold blood can increase the risk of hypothermia in an already critically injured patient.

Once warmed, the blood is typically wrapped in simple insulation with hand warmers, attached to a drone, flown toward the front, and dropped to the receiving soldiers without requiring the drone to land.

For a soldier experiencing severe blood loss, those extra minutes can be critical.

**Ten minutes spent waiting for blood to warm can be the difference between the transfusion arriving in time or arriving too late.**

---

## Goal

Our challenge was to reduce the time between a soldier requesting blood and receiving it by **combining blood warming and drone transportation into one process**.

Instead of waiting for the blood to warm before launch, the drone could leave almost immediately while the blood warmed during the flight.

### Existing Process

**Cold Blood → Wait to Warm → Package → Drone Flight → Patient**

### Our Goal

**Cold Blood → Activate Warmer → Warm During Drone Flight → Patient**

Rather than beginning with a technology we wanted to use, we first focused on understanding the people who would interact with the device and the environment in which it would operate.

This became the core of our **human-centered design process**.

---

## Human-Centered Design

We identified the stakeholders, design constraints, and functional requirements that would determine whether a solution could realistically work in the field.

![Project Team](/assets/img/Blood2.png)

Conversations with our project sponsor changed several of our early assumptions.

Initially, we considered powered systems using heaters, sensors, batteries, and electronic controls. From a traditional engineering perspective, these solutions offered excellent temperature control.

In a war zone, however, every additional component is something that can be **lost, damaged, unavailable, or impossible to replace**.

That led us to a better question:

### **How can we remove as much complexity as possible?**

Taking these constraints into account, we established our final design goal:

> **Develop a battery-free device that can warm blood from approximately 4°C to at least 25°C during a 10-minute drone flight while weighing less than 2 kg, reclaiming the 10–12 minutes currently spent warming blood before launch.**

---

## Ideate Phase

Once we clearly defined the problem, each team member independently generated potential solutions using sticky notes.

We then grouped the ideas by similarity and used **dot voting** to identify the concepts that best addressed our functional requirements and design constraints.

![Ideation and Dot Voting](/assets/img/Blood3.png)

Two concepts emerged as our strongest options.

---

## Top Concept One: Grain-Filled Microwave Pouch

Our first concept took inspiration from reusable microwavable heating pads.

Instead of a traditional rectangular heating pad, the design would act as an insulated pouch capable of holding two blood bags. Materials such as grain or clay beads would be heated before use, retaining heat while also providing cushioning during the drone flight.

The design had several advantages:

- Simple construction
- Easily available materials
- Reusable
- Added impact protection for the blood bags

However, we had concerns about **weight, heat retention, and dependence on access to a microwave**.

![Project Team](/assets/img/Blood4.png)

---

## Top Concept Two: Exothermic Reaction Sleeve

Our second concept used a sealed pouch containing an **activated exothermic heating system**.

The blood bag would sit between two heating panels, allowing heat to transfer into the blood during transportation.

Unlike the microwave pouch, an exothermic heater could be activated almost immediately and continue generating heat throughout the drone flight without requiring electrical power.

The main challenge became **temperature control**.

The system needed to generate enough heat to warm the blood quickly without allowing the blood to overheat and potentially degrade.

![Exothermic Reaction Sleeve Concept](/assets/img/Blood5.png)

---

## Initial Testing

After selecting our two strongest concepts, we began experimentally comparing their performance.

We used **two thermocouples connected to a DAQ board** to record temperature during each test. Instead of real blood, we filled medical-grade blood bags with a **40% glycerol and 60% water solution** to approximate the thermal behavior required for our testing.

![Initial Testing Results](/assets/img/Blood6.png)

The grain-filled microwave pouch increased the simulated blood temperature by approximately **10°C**, while the reusable HotSnapZ hand warmers produced an increase of approximately **17°C**.

The larger temperature increase from the chemical heating method encouraged us to continue developing the **exothermic reaction concept**.

---

## Developing the Design

Through additional testing, we moved from reusable HotSnapZ hand warmers to **MRE flameless ration heaters**.

MRE heaters offered several important advantages:

- Single-use
- Battery-free
- Lightweight
- Already associated with military supply chains
- Consistently capable of producing higher temperatures

Rather than inventing an entirely new heat source, we began adapting an existing technology for a new medical transportation application.

We fabricated a **plastic mesh pouch** capable of holding two MRE heaters and one blood bag. The mesh was durable and water resistant while still allowing heat to transfer toward the blood bag without placing the heaters directly against it.

![Blood Warmer Prototype Development](/assets/img/Blood7.png)

---

## Final Design

Our final proof-of-concept used a **three-layer system** centered around the water-activated exothermic reaction of flameless ration heaters.

![Project Team](/assets/img/Blood8.png)

### Layer 1: Mesh Heating Pouch

The innermost bag is made from white plastic mesh and contains three compartments:

- One large center compartment for the blood bag
- Two smaller side compartments for the MRE heaters

Each heater compartment uses a Velcro closure so the heaters can be inserted quickly after activation.

Each MRE heater is activated using approximately **10 mL of water**.

### Layer 2: Quilted Protective Pouch

Once the blood bag and two activated MRE heaters are secured in the mesh pouch, the assembly is placed inside a **quilted, water-resistant pouch**.

This layer provides additional insulation and protects the blood bag during transportation and the drone drop.

### Layer 3: Insulated Outer Bag

The complete assembly is then placed inside an **insulated outer bag** to retain heat during flight.

The package can then be attached underneath the drone and transported toward the injured soldier while the blood warms.

---

## Results

After multiple prototype iterations and tests, our final design consistently warmed the simulated blood from below **8°C to above 25°C in 15 minutes or less** while remaining lightweight, simple, and completely battery-free.

![MRE Blood Warmer Test Results](/assets/img/Blood10.png)

More importantly, the system allowed **warming and transportation to happen at the same time**.

### Existing Process

**Warm Blood in Water Bath:** ~12 minutes  
**Drone Transport:** ~15–20 minutes  

**Total Process:** approximately **32 minutes**

### Proposed Process

**Activate Warmer & Package Blood:** ~1 minute 30 seconds  
**Warm Blood During Drone Transport:** ~15–20 minutes  

**Total Process:** approximately **20.5 minutes**

### **Over 30% Reduction in Total Process Time**

The most important result was not simply that we successfully warmed the simulated blood.

We removed an entire waiting step from the emergency blood-delivery process.

Instead of:

**Warm → Fly**

our design allows the system to:

### **Warm + Fly**

---

## Reflection

This project changed the way I think about engineering design.

At the beginning, it was tempting to approach the problem by asking:

### **What is the best way to heat blood?**

Human-centered design led us to a better question:

### **What does the person trying to get blood to an injured soldier actually need?**

The most technologically sophisticated solution was not necessarily the best solution.

A battery-powered heater with sensors and precise electronic controls might perform extremely well in a laboratory, but it becomes much less useful if a damaged supply chain makes replacement batteries unavailable or if an expensive reusable device is lost with a drone.

Our final concept was intentionally simple because **simplicity itself became an engineering requirement created by the people and environment we were designing for**.

This project gave me experience with **human-centered design, stakeholder analysis, concept generation, engineering trade studies, rapid prototyping, experimental testing, thermal system design, and iterative product development**.

More importantly, it reinforced that good engineering starts with understanding the real problem—not simply building the most technically impressive solution.

This project was an **academic proof of concept rather than a clinically validated medical device**, and significant medical and engineering validation would be required before any real-world implementation. I am proud that the concept has since been **further pursued through Vanderbilt research**.

---

## Additional Project Research

As part of the human-centered design process, we researched the variety of drones operating in Ukraine and the conditions that influence how equipment can be transported and resupplied.

<div class="blood-two-column">
  <img src="/assets/img/Blood11.png" alt="Types of drones used in Ukraine">
  <img src="/assets/img/Blood12.png" alt="Drone warfare research in Ukraine">
</div>

The variety of FPV drones, reconnaissance aircraft, and modified commercial quadcopters reinforced an important design requirement: our solution could not depend on one specific drone platform.


