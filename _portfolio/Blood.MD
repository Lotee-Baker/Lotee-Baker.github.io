---
title: "Drone-Delivered Exothermic Blood Warmer"
excerpt: "Using human-centered design to merge blood warming and drone transport for faster emergency transfusions on the Ukrainian front"
categories:
  - Design Engineering
  - Research and Experimental
header:
  image: /assets/img/BloodWarmer1.jpeg
  teaser: /assets/img/BloodWarmer1.jpeg
---

**Role:** Mechanical Engineering Student, Interdisciplinary Design Team  
**Course:** How to Make Anything and Make It Matter  
**Focus:** Human-Centered Design, Rapid Prototyping & Experimental Testing  

---

## Project Overview

This project started with a deceptively simple question:

**How can we get warm blood to an injured soldier faster?**

For our *How to Make Anything and Make It Matter* course, my team worked with **Tim Bongartz, Assistant Professor of Emergency Medicine and Associate Medical Director for the Metro Nashville Police Department SWAT team**, to investigate a challenge currently faced in Ukraine.

Whole blood must be kept cold during storage, but transfusing very cold blood into a trauma patient can contribute to hypothermia and impair coagulation. The blood therefore needs to be warmed before it reaches an injured soldier.

The problem was not simply how to warm blood.

The problem was **when** it was being warmed.

---

## The Problem in Ukraine

The war in Ukraine has created a battlefield unlike almost any that came before it in its dependence on small unmanned aircraft.

Commercial quadcopters, FPV drones, reconnaissance UAVs, and purpose-built military drones are used throughout the battlefield. Different units may use completely different aircraft, and drones are regularly modified, jammed, damaged, or shot down.

That makes them more than weapons—they have also become a way of moving critical resources across areas where sending a person or vehicle may be extremely dangerous.

One of those resources is **blood**.

At the drone stations we studied, blood is stored refrigerated behind the front line. When a soldier needs an emergency transfusion, the existing process requires the operators to:

**Remove Blood from Refrigeration → Warm Blood → Package Blood → Load Drone → Fly to Front Line → Drop Blood to Soldiers**

The warming step alone can add roughly **10–12 minutes before the drone even leaves**.

The blood is then placed in simple insulation such as bubble wrap and hand warmers, attached to a drone, flown toward the front, and dropped to the receiving soldiers without the drone needing to land.

For a critically injured soldier experiencing severe blood loss, those extra minutes matter.

**Ten minutes spent waiting for blood to warm can be the difference between the transfusion arriving in time or arriving too late.**

---

## Reframing the Problem

One of the most important moments in our design process came when we stopped thinking of **warming** and **transportation** as two separate operations.

Why warm the blood for ten minutes...

and *then* fly it for another ten to twenty minutes?

The drone flight itself was unused time.

Our design challenge became:

> **Develop a lightweight, battery-free system that warms refrigerated blood during drone transport rather than before it.**

By combining these two processes, the drone could leave almost immediately while the blood warmed in the air.

**Old Process:**  
Cold Blood → **Wait to Warm** → Drone Flight → Patient

**Our Goal:**  
Cold Blood → **Warm During Drone Flight** → Patient

This reframing became the foundation of the project.

---

## Human-Centered Design

Rather than beginning with a technology we wanted to use, we started by understanding the people who would actually interact with the device.

Our major stakeholders included:

- **Injured soldiers**, who ultimately depend on the blood arriving quickly and safely.
- **Combat medics and responding soldiers**, who need a simple device that requires little training or setup.
- **Drone operators**, who need to load and launch the blood quickly.
- **Logistics personnel**, who operate with disrupted and unpredictable supply chains.
- **Medical personnel**, who need the blood to remain within a safe temperature range.

Conversations with our project sponsor changed several of our early assumptions.

For example, we originally considered powered systems with heaters, sensors, batteries, and electronic controls. From a traditional engineering perspective, these offered excellent temperature control.

From the perspective of someone operating in a war zone, however, every additional component was another component that could be lost, damaged, unavailable, or impossible to replace.

The better question became:

**How can we remove as much complexity as possible?**

---

## Designing for a War Zone

The environment drove our engineering requirements.

The device needed to be:

- **Battery-free** so it did not depend on charging infrastructure or replacement batteries.
- **Lightweight** so the drone could still carry useful quantities of blood.
- **Low-cost** because the device or the drone carrying it could be lost.
- **Simple to activate** under stressful conditions.
- **Adaptable** to different drone platforms.
- **Fast**, beginning the warming process almost immediately.
- **Protective**, because the blood could be dropped from the hovering drone.
- **Safe**, preventing the blood from overheating.

Our target was to warm refrigerated blood from approximately **4°C to at least 25°C during transport**, while keeping the complete system below **2 kg**.

The design also needed to accommodate typical **300–500 mL blood bags** and drones with payload capacities of only a few kilograms.

---

## Ideation

We intentionally explored a wide range of solutions before choosing a direction.

Our concepts included:

- Grain-filled microwave heating pouches
- Rechargeable warming belts
- Flexible electric heating elements
- Heated metal sleeves
- Blood pumps with heated tubing
- Hand-warmer-based insulation
- Air-activated heaters
- Exothermic reaction sleeves
- Drone-mounted heating systems

We grouped similar ideas, compared powered and non-powered approaches, voted on promising concepts, researched existing technologies, and used **Go/No-Go screening** and technology-readiness considerations to narrow the field.

Three concepts emerged as our strongest options:

### Grain-Filled Heating Pouch

A reusable insulated pouch containing microwave-heated material such as flax seed, millet, or clay beads.

It was simple and reusable, but retaining enough heat while staying lightweight was a concern.

### Electrically Heated Metal Mesh

A thin resistive heating system capable of distributing heat evenly around the blood bag.

This offered excellent temperature control, but required electrical power, sensors, and additional components—the exact dependencies we were trying to eliminate.

### Exothermic Reaction Sleeve

A lightweight sleeve that generates heat through a chemical reaction.

It could be **battery-free, inexpensive, fast to activate, and independent of the drone's electrical system**.

That made the exothermic approach the best fit for the environment we were designing for.

---

## Prototype & Test

Our first prototypes used commercially available hand warmers surrounding a simulated blood bag.

To safely experiment without using real blood, we tested using liquids selected to approximate the thermal behavior of the blood bag.

One prototype used four reusable **HotSnapZ hand warmers** wrapped around the bag.

The result was encouraging—but not enough.

The simulated blood increased by approximately **17°C**, while our desired temperature change was closer to **26°C**.

We needed a stronger heat source.

---

## Learning from an Existing Military Technology

We next looked at something already designed to be lightweight, inexpensive, portable, and usable without electricity:

**Flameless ration heaters used in MREs.**

The same exothermic reaction normally used to heat a soldier's meal could potentially heat a blood bag during a drone flight.

Testing showed that the MRE heaters produced significantly more heat than the hand warmers.

That created a new problem:

**They could become too hot.**

Heating faster was useful, but blood cannot simply be exposed to the highest temperature possible. We now needed to control the heat transfer between the exothermic reaction and the blood bag.

---

## Iterating the Design

Our prototype evolved into a layered system.

The blood bag was surrounded by the exothermic heaters, while additional layers separated, protected, and insulated the system.

Our testing setup incorporated:

- The simulated blood bag
- Two MRE heaters
- A mesh layer
- A quilted protective pouch
- An insulated outer bag

The design served several purposes at once.

The outer insulation retained heat during transport, the protective layers cushioned the blood bag, and the inner layers reduced direct exposure to the hottest areas of the exothermic heaters.

Instead of designing an entirely new heating technology, we adapted an **existing, inexpensive and field-proven heat source** to solve a very different problem.

---

## Results

Our most recent prototype heated the simulated blood from approximately:

**6°C → 25°C in 15 minutes**

while remaining **lightweight, simple, and completely battery-free**.

More importantly, the prototype allowed the warming and transportation processes to happen at the same time.

### Existing Process

**Warm Blood in Water Bath:** ~12 minutes  
**Drone Transport:** ~15–20 minutes  

**Total Process:** approximately **32 minutes**

### Proposed Process

**Activate Warmer & Package Blood:** ~1 minute 30 seconds  
**Warm Blood During Drone Transport:** ~15–20 minutes  

**Total Process:** approximately **20.5 minutes**

That represents an **over 30% reduction in total process time**.

The important result was not simply that we built something capable of warming a blood bag.

It was that we eliminated an entire step from the emergency response process.

---

## Why 10 Minutes Matters

In most engineering projects, saving ten minutes might simply mean making a process more efficient.

Here, the stakes are very different.

A soldier requiring an emergency blood transfusion may already be experiencing severe hemorrhage, hypothermia, and rapidly decreasing chances of survival.

The existing process uses valuable time warming blood while the drone remains on the ground.

Our design turns that same period into productive transport time.

Instead of:

**Warm → Fly**

the system allows us to:

**Warm + Fly**

That small change in how the problem is framed can potentially move life-saving blood toward the patient **roughly ten minutes sooner**.

---

## Future Development

This project was an academic proof-of-concept rather than a clinically validated medical device, and several important questions would need to be addressed before real-world use.

Our next steps included:

- Testing the system in **cold outdoor conditions** representative of Ukrainian winters.
- Better controlling the temperature at the **heater-to-blood interface**.
- Testing thin **aluminum or graphite layers** to distribute heat more evenly.
- Adding **color-changing temperature indicators** so users can quickly identify whether the blood is within the desired range.
- Continuing to reduce weight and setup time.
- Testing packaging capable of better protecting the blood during a drone drop.
- Performing substantially more thermal and medical validation before any clinical application.

---

## Reflection

This project changed the way I think about engineering design.

At the beginning, it was tempting to approach the problem by asking:

**What is the best way to heat blood?**

Human-centered design forced us to ask a better question:

**What does the person trying to get blood to an injured soldier actually need?**

The technically most sophisticated solution was not necessarily the best solution.

A battery-powered heater with sensors and precise electronic control might perform extremely well in a laboratory, but it becomes far less useful if a damaged supply line prevents someone from replacing the battery or a drone carrying an expensive reusable device is shot down.

The final concept was intentionally simple because **simplicity was an engineering requirement created by the people and environment we were designing for**.

This project gave me experience with **human-centered design, stakeholder analysis, concept generation, engineering trade studies, rapid prototyping, experimental testing, thermal system design, and iterative product development**.

More importantly, it reinforced that good engineering starts with understanding the real problem—not simply building the most technically impressive solution.
