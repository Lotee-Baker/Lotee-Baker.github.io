---
title: "Minature Laser Alarm System"
excerpt: "A minture art room with a laser alarm system to protect Barry the Red Dinosour"
header:
  image: /assets/img/Laser8.jpeg
  teaser: /assets/img/Laser8.jpeg
gallery:
  - image_path: /assets/img/Laser1.jpeg
  - image_path: /assets/img/Laser2.jpeg
  - image_path: /assets/img/Laser3.jpeg
  - image_path: /assets/img/Laser4.jpeg
  - image_path: /assets/img/Laser5.jpeg
  - image_path: /assets/img/Laser6.jpeg
  - image_path: /assets/img/Laser7.jpeg
  - image_path: /assets/img/Laser8.jpeg
  - image_path: /assets/img/Laser9.jpeg
  - image_path: /assets/img/Laser10.jpeg
  - image_path: /assets/img/Laser11.jpeg
---


# Laser Alarm System


**Course Project:** Mechatronics Final Project
**Role:** Designer & Builder
**Timeline:** Semester Project


---


## Project Overview
For my mechatronics final, I wanted to create something that felt straight out of *Mission Impossible*. The result? A **laser alarm system** that guarded my 3D-printed dinosaur (*Barry*) like it was sitting in a high-security museum display.

![Barry the Red Dinosaur](/assets/img/Laser1.jpeg)

The system detects intruders with a laser grid, slams a servo-powered door shut to protect the object, blares an alarm, and flashes a scrolling warning on an LCD screen. After a one-minute “lockdown,” the system resets itself and gets ready for the next daring thief.


---


## Design & Development
- **Laser Grid:** I started ambitious at an eight laser design but quickly realized my Arduino couldn’t handle that many inputs and power demands so I scaled back to three. It still gave that “heist movie” effect while staying reliable.
- **Protective Door:** I built a lightweight door out of cardboard and attatched it to a servo motor. This servo motor snapped shut whenever the laser beams were broken. I powered it with its own 9V battery so it wouldn’t overload the Arduino.
- **Alarm & Display:** A buzzer screamed when the system was triggered, and the 20x4 LCD scrolled “ALARM TRIGGERED” across the screen. I had to learn how to use a new Arduino library to pull this off.
- **Enclosures:** I modeled housings in Fusion 360 for the display box and alarm box, laser-cut the pieces in 1/4th" MDF, and wrapped them in black fabric to give the final project a polished, showcase-ready look.


---


## What I Learned
- Sometimes you have to **scale back big ideas** (eight lasers!) to get something working reliably.
- Debugging is everything — aligning those laser beams was more finicky than I expected.
- Integrating electronics, mechanics, and software is messy, but also incredibly rewarding.


---


## Skills Demonstrated
- Arduino programming (servo control, LCD libraries, sensor logic)
- CAD design and laser cutting (Fusion 360 + fabrication)
- Prototyping & system integration
- Balancing creative ambition with practical execution


---


## Results
The final build worked exactly as planned: Barry stayed safe, the alarm looked and sounded dramatic, and the system could reset and run multiple times. It was easily one of the most fun projects I’ve worked on because it combined **engineering with storytelling** — something I’m passionate about carrying into my future projects in mechanical and themed entertainment design.


---

<style>
.image-grid {
display: grid;
grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
gap: 12px;
}
.image-grid img {
width: 100%;
height: auto;
border-radius: 10px;
}
blockquote { border-left: 4px solid #7a8899; padding-left: 12px; color: #495268; }
</style>


---

{% include gallery caption="Phone Holder" %}
