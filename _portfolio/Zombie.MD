---
title: "Zombie Animatronic"
excerpt: "A Zombie Animatronic Addition to Flag Tag AZ's laser tag arena"
header:
  image: /assets/img/micro1.jpeg
  teaser: /assets/img/micro1.jpeg
gallery:
  - url: /assets/img/micro1.jpeg
    image_path: /assets/img/micro1.jpeg
    alt: "placeholder image 1"
---
# Interactive Zombie Head Animatronic Installation
As an independent contractor, I designed and installed an interactive zombie head animatronic for a laser tag arena in Flagstaff, AZ. The goal was to create an engaging target for players to shoot while staying within budget.

# Design and Development:
I conceptualized an interactive component that fit within the size constraints of the tank. I also reinforced the tank's existing structural supports to ensure stability.

## 2. Print and Cure Mold
Once the Fusion 360 model was finished, it was put into Preform, a 3D slicing software, and printed on a Formlabs Form 3 SLA 3D printer in black resin. After the mold was printed it was put in an isopropyl alcohol bath for 10 minutes with the supports on. Then the supports were taken off and the mold was washed again in isopropyl alcohol for another 5 minutes. After this, the mold was tilted against a wall so that the alcohol could flow out and left to dry for 30 min. Once dried, the mold was checked for any uncured resin as uncured resin could lead to further complications in the demolding process. If there is no uncured resin the mold will have a homogeneous sheen. Once confirmed that there was no uncured resin, the mold was cured under UV light at 60 degrees celsius for 1 minute. 

## 3. Parylene Coating of the Mold
The 3D printed mold cannot be immediately cast with PDMS. First, you have to coat the mold in a thin layer of parylene. Parylene is a biocompatible polymer and is vapor deposited onto the mold in a vacuum chamber.

![Microfluidic Mold](/assets/img/micro2.jpeg)

## 4. Cast PDMS
Now that the mold is coated, it can now be casted in PDMS. PDMS is a common material for microfluidic devices because of its biocompatibility and its flexibility. It is mixed in a 10:1 ratio of base to curing agent and is degassed in a vacuum chamber to remove air bubbles. Once this is done, the PDMS is poured into the coated mold and baked at 60 degrees celsius for several hours to ensure a full cure. After the cast is fully cured it is peeled from the mold and is ready for the next step. 

## 5. Plasma Bonding to Glass Slide
The final step to create this LoC particle sorting device is to bond the PDMS microfluidic cast to a glass slide. The glass slide is very important for this device because it gives the PDMS cast something rigid to adhere to. It also seals off all of the channels in the microfluidic device. 

To bond the two together, the PDMS cast and the glass slide are placed in a plasma chamber. In this chamber they are exposed to oxygen plasma that increases the surface energy of both materials. This makes them super adhesive and perfect for bonding. Then the PDMS cast and the glass slide are aligned and pressed together for a few minutes until they are strongly bonded together. After the glass slide and the PDMS cast are bonded the microfluidic Lab-on-Chip particle sorter is ready for use. 

# Discussion 
## Why is the resin mold coated in Parylene? 
Even after curing under UV light, the resin print has uncured resin monomers. If the PDMS is poured directly onto the resin print, then these monomers can leach into the PDMS and cause the PDMS to not cure correctly resulting in a loss of features or just a completely uncured cast. The Parylene coating prevents this leaching and enhances the overall surface smoothness allowing for an easier demolding process and more laminar flow in the microfluidic device. The Parylene also increases the durability of the mold allowing for multiple casts and a longer use. 

## What could we use this device for?
This is an important question because it is important to know a device's function while designing it. For example, if I was creating this particle sorting device to isolate tumor cells from a blood stream I would prioritize biocompatibility and set my outlets to catch the particle size of the tumor cells. These are all decisions that have to be made in the fabrication process and cannot be altered once the device is made.  

## Why is my design conducive to sorting? 
This microfluidic device is designed to sort two particle size ranges: 125–150 μm and 425–500 μm. The pinch width was set at 0.75 mm, as a smaller pinch width increases particle spreading, making separation more effective. This value was chosen because it is 1.5 times the size of the largest expected particle, ensuring that particles do not get stuck in the channel while still achieving effective separation. The wider channel width was set at 19 mm, as a larger width allows for greater particle dispersion, improving sorting efficiency. However, the width could not be increased further due to the requirement for a 3 mm bonding margin between the PDMS cast and the glass slide to ensure a secure seal.

Once the pinch width and overall channel width were determined, the expected positions of the sorted particles were calculated. The average position for the smaller particles was determined to be 17.26 mm, while the position for the larger particles was 13.14 mm. To center these positions within the outlets, fluid separators were placed at 15.2 mm, with the next separator positioned 3.8 mm below that. This design maximizes particle spreading while minimizing the risk of clogging.

For the outlets, the barbs used in this device have a diameter of 11 mm, requiring the outlets to be spaced 11 mm apart to ensure proper fluid connections. These carefully chosen dimensions allow for efficient sorting while preventing clogging, ensuring that the device remains functional and effective in continuous particle separation applications.

## Does each outlet have the same flow rate? 
This design decision was crucial because all outlets could not have been placed equidistant from the separation region due to the 11 mm barbs, I instead positioned two outlets 37 mm from the separation region and the other two outlets 24.5 mm away. This 10.5 mm difference could create unequal flow resistances, leading to varying flow rates among the channels. Unequal flow rates can shift particle trajectories at the last moment, causing particles to enter the channel with the highest flow rate, which would result in unreliable sorting and potentially render the device unusable.

To address this issue, I adjusted the channel widths to balance the flow distribution. The top two channels were made 0.67 mm wide, while the bottom two channels were 1 mm wide, ensuring that the top channels accommodate 67% of the liquid volume compared to the bottom channels. Additionally, to equalize the effective channel lengths, I introduced curved outlet paths for the shorter channels. Each curve has a radius of 5 mm and spans 128 degrees of a circle, resulting in a total path length of 34.75 mm, which closely matches the 37 mm target. I intentionally made the curved paths slightly shorter to compensate for the added resistance caused by the bends. These design choices ensure that all outlets maintain similar flow rates, improving sorting accuracy and device reliability.

## Results 
During testing, a significant issue was identified with the outlet flow. If the tubes connected to the outlets were positioned at slightly different heights, they created unequal flow resistances, preventing the device from effectively sorting particles. To address this, I would implement an improvement by 3D-printing rigid tubes that could be attached to the outlet barbs. These tubes would be identical in dimensions, ensuring that each outlet maintains consistent flow resistance and, consequently, equal flow rates, allowing the device to function reliably.





{% include gallery caption="This is a sample gallery to go along with this case study." %}
