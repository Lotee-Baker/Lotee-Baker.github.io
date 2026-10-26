---
title: "Drone Delivered Exothermic Blood Warmer"
excerpt: "Developing a lightweight, battery free blood warmer for emergency drone delivery to injured Ukrainian soldiers"
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

For our *How to Make Anything and Make It Matter* course, my team partnered with **Tim Bongartz** to investigate emergency medicine challenges currently faced in Ukraine. Tim spent time with Ukrainian soldiers near the front lines and identified a core area for improvement in their emergency medicine process that became the heart of our project:

### **Injured Ukrainian Soldiers Need Warm Blood Fast in an Unprecedented Drone War Zone**

![Project Team](/assets/img/Blood1.png)

---

## Project Background

The war in Ukraine has created a battlefield unlike almost any that came before it in its dependence on small unmanned aircraft. Different units may use completely different aircraft, and drones are regularly modified, jammed, damaged, or shot down.

These drones are also used to deliver warmed blood to injured soldiers in otherwise unreachable areas.

At the drone stations, blood is refrigerated behind the front line. When a soldier needs an emergency transfusion, the existing process requires the operators to:

**Remove Blood from Refrigeration → Warm Blood in a Water Bath → Package Blood → Load Drone → Fly to Front Line → Drop Blood to Soldiers**

The warming step alone can add roughly **10–12 minutes before the drone even leaves**, but it is essential to reduce the risk of hypothermia for the injured soldier.

Once warmed, the blood is placed in simple bubble wrap insulation with hand warmers, attached to a drone, flown toward the front, and dropped to the receiving soldiers without the drone needing to land.

For a critically injured soldier experiencing severe blood loss, those extra minutes can be the difference between life and death.

### **Ten minutes spent waiting for blood to warm can be the difference between the transfusion arriving in time or arriving too late.**

---

## Goal

To reduce the time between when a soldier calls for blood and receives it by drone, we were asked to **combine the blood warming and transportation processes into one**.

By combining these two processes, the drone could leave almost immediately while the blood warmed in the air.

Rather than beginning with a technology we wanted to use, we started by understanding the people who would interact with the device. We had to accurately identify our **stakeholders, design constraints, and functional requirements**.

This is the core of **human centered design**.

![Project Team](/assets/img/Blood2.png)

Conversations with our project sponsor changed several of our early assumptions.

For example, we originally considered powered systems with heaters, sensors, batteries, and electronic controls. From a traditional engineering perspective, these offered excellent temperature control.

From the perspective of someone operating in a war zone, however, every additional component was another component that could be **lost, damaged, unavailable, or impossible to replace**.

The better question became:

### **How can we remove as much complexity as possible?**

With all of this taken into account, we set our goal:

> **Develop a battery-less device that can warm blood from approximately 4°C to a minimum of 25°C during a 10 minute drone flight while weighing under 2 kilograms, reclaiming those valuable 10–12 minutes.**

---

## Ideate Phase

Once we clearly defined our goal, we individually came up with multiple ideas on sticky notes, separated them into categories, and used the **dot-voting method** to identify our favorite ideas.

![Ideate Phase](/assets/img/Blood3.png)

Two concepts stood out as our strongest options.

---

## Top Concept One: Grain Filled Microwave Pouch

This device took inspiration from reusable microwavable heating pads that are already on the market.

However, instead of a rectangular heating pad, it would be a pouch that could contain two blood bags, retain heat, and cushion the blood bags during their drone journey.

This solution would be easily reproducible using common materials such as grain, clay beads, and fabric, while also providing padding for the blood bags during transportation.

However, we had concerns about **weight, heat retention, and dependence on a microwave**.

![Project Team](/assets/img/Blood4.png)

---

## Top Concept Two: Exothermic Reaction Sleeve

Our second concept was a sealed pouch containing an activated **exothermic sleeve**.

This simple sleeve would be composed of two panels that quickly heat the blood bag placed between them.

Unlike the first concept, this solution could be activated almost instantly and would continue producing heat throughout the drone's flight.

However, with this solution, we had to make sure that the blood would **not overheat and begin to degrade**.

![Exothermic Reaction Sleeve Concept](/assets/img/Blood5.png)

---

## Initial Testing Results

After deciding on the two main concepts to move forward with, we performed initial testing using **two thermocouples connected to a DAQ board**.

For our simulated “blood,” we used a **40% glycerol and 60% water solution** inside medical grade blood bags to create comparable heat transfer behavior for testing.

![Initial Testing Results](/assets/img/Blood6.png)

These results led us to move forward with the **exothermic reaction concept**, as it produced a larger increase in temperature.

---

## Developing the Design

Through further testing, we moved from HotSnapZ hand warmers to **MRE ration heaters**.

MRE heaters were appealing because they are:

- Single use
- Battery free
- Already associated with military supply chains
- Lightweight
- Able to consistently warm the blood to higher temperatures

After confirming the source of our exothermic reaction, we fabricated a **mesh pouch** to hold two MRE ration heaters and one blood bag.

This plastic mesh was durable, water resistant, and still allowed heat to transfer into the blood bag without placing the heaters in direct contact with it, helping reduce the risk of overheating the blood.

![Project Team](/assets/img/Blood7.png)

---

## Final Design

Instead of designing an entirely new heating technology, we adapted an existing, inexpensive heat source to solve our problem.

Our solution is a **three bag method** that uses the water triggered exothermic reaction of flameless ration heaters.

![Project Team](/assets/img/Blood8.png)

The first bag is made from **white plastic mesh** and contains three compartments:

- One large middle compartment for the blood bag
- Two smaller side compartments for the MRE heaters

The side compartments have Velcro strips so soldiers can quickly insert the MRE heaters after activating each one with approximately **10 mL of water**.

Once the mesh bag contains one blood bag and two activated MRE heaters, it is placed inside a **quilted, water-resistant pouch** to provide additional padding and insulation for the drone transportation and drop.

The entire assembly is then placed inside an aluminium **insulated outer bag** and is ready to be attached underneath the drone and flown toward the injured soldier.

---

## Results

<video width="100%" autoplay muted loop playsinline>
  <source src="/assets/img/Blood.mp4" type="video/mp4">
</video>

After multiple tests, our most recent prototype was able to heat the simulated blood from below **8°C to above 25°C in 15 minutes or less** while remaining lightweight, simple, and completely battery free.

![MRE Trial Data](/assets/img/Blood9.png)

More importantly, the prototype allowed the **warming and transportation processes to happen at the same time**.

### Existing Process

**Warm Blood in Water Bath:** ~12 minutes  
**Drone Transport:** ~15–20 minutes  

**Total Process:** approximately **32 minutes**

### Proposed Process

**Activate Warmer & Package Blood:** ~1 minute 30 seconds  
**Warm Blood During Drone Transport:** ~15–20 minutes  

**Total Process:** approximately **20.5 minutes**

### **That represents an over 30% reduction in total process time.**

---

## Reflection

This project changed the way I think about engineering design.

At the beginning, it was tempting to approach the problem by asking:

### **What is the best way to heat blood?**

Human centered design forced us to ask a better question:

### **What does the person trying to get blood to an injured soldier actually need?**

The technically most sophisticated solution was not necessarily the best solution.

A battery powered heater with sensors and precise electronic controls might perform extremely well in a laboratory, but it becomes far less useful if a damaged supply line prevents someone from replacing the battery or if a drone carrying an expensive reusable device is shot down.

The final concept was intentionally simple because **simplicity was an engineering requirement created by the people and environment we were designing for**.

This project gave me experience with **human centered design, stakeholder analysis, concept generation, engineering trade studies, rapid prototyping, experimental testing, thermal system design, and iterative product development**.

More importantly, it reinforced that good engineering starts with understanding the real problem, not simply building the most technically impressive solution.

This project was an **academic proof of concept rather than a clinically validated medical device**, and several important questions would still need to be addressed before real world use.

I am proud to say that this project has since been **further pursued by Vanderbilt's research facilities**.

---

## Supplemental Research

As part of the project, we also researched the different types of drones being used in Ukraine and how drone warfare affects the design requirements of the blood warmer.

<div class="blood-two-column">
  <img src="/assets/img/Blood11.jpeg" alt="Different combat drones used in Ukraine">
  <img src="/assets/img/Blood12.jpeg" alt="Drone warfare research">
</div>

Because different Ukrainian units may operate completely different aircraft, our solution needed to remain **independent of any specific drone platform**.

We also reviewed the existing heating method used in the field to understand exactly what parts of the process our design needed to improve.

![Current Blood Heating Method](/assets/img/Blood13.jpeg)
