---
title: "Phone Holder"
excerpt: "Realiable, Low Profile, 3D Printed Phone Holder for a Bike or Scooter"
header:
  image: /assets/img/Pliers.jpg
  teaser: /assets/img/Pliers.jpg
gallery:
  - url: /assets/img/Pliers.jpg
    image_path: /assets/img/Pliers.jpg
    alt: "placeholder image 1"
  - url: /assets/img/failed pliers.jpg
    image_path: /assets/img/failed pliers.jpg
    alt: "1st Iteration of Pliers: Dove Tails too small"
  - url: /assets/img/Thingaverse Pliers.jpg
    image_path: /assets/img/Thingaverse Pliers.jpg
    alt: "Pliers Example on Thingaverse"
  - url: /assets/img/Flexi Rex.jpg
    image_path: /assets/img/Flexi Rex.jpg
    alt: "Flexi Rex"
  - url: /assets/img/slug.jpg
    image_path: /assets/img/slug.jpg
    alt: "Friendly Articulated Slug"
---
# The Goal 
The goal of this design was to create a low profile phone holder that can affix to the handlebars of a bike or scooter and easily rotate between landscape and portrait mode. Like any good phone holder you should be able to quickly attach and detach your phone on the go and the phone should have no risk of falling out on a bumpy ride. 

# The Design 
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a41e340cb8bc464afd?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

The first component of the design is the clamp that affixes to the handle bars. I mentioned this briefly earlier but the clamp is a simple 2 body design that is 0.25 mm offset from the diameter of the handle bar and bolted together with m6 bolts. The next challenge of this design was how the holder was going to rotate between landscape and portrait mode. My first idea was to have a compression spring connected between the clamp and the phone holder so that you could pull the holder out, rotate it 90 degrees, and put it back in but this design had multiple issues. First, it created a bulky clamp as it needed a long neck for the compression spring and second, it wasn't very secure. The design I ended up going with was a detent mechanism with two spring loaded balls. This worked significantly better than my first idea as it was much more low profile and secure because the holder and the clamp were affixed together with a bolt instead of a spring. For the detent mechanism, the clamp held the springs and the balls and the phone holder had circular notches at 0, 90, 180, and 270 degrees that the balls will snap into when the holder is rotated. This was a minimal but effective solution that allowed for the phone to rotate easily between landscape and portrait. To hold the phone, the phone holder was designed with two parts. One main body that had a flat plane and walls for the sides of the phone and a band that wraps around the top and the bottom to hold it into place. During my design I made sure none of my features were smaller than 0.6 mm so that they could be printed accurately and gave around 0.3 mm of tolerance for my bolt holes to account for the printer’s tolerance.  

# Printing 

I printed all of my components on FFF printers for their speed and their ability to print PLA and TPU. I printed both parts of the clamp, and the main part of the phone holder in PLA with 15% infill and I printed the band attachment to the phone holder in TPU with the “vase mode” slicer setting for reliable elasticity. 

# Assembly 

To attach the clamp to the handle bars, both sides were put together around the handlebar and bolted together with m6 bolts. Then the springs and balls were put into their notches on the top clamp. The TPU band was stretched around the bottom of the main phone holder body until it slipped into the notch in the neck of the holder.After this, the phone holder was pushed into the circular hole in the top part of the clamp compressing the springs between the top clamp and the phone holder. Then the phone holder and the top clamp were bolted together with a m6 bolt. It is important to note that this bolt wasn't tightened all the way so that the phone holder could still rotate around it. 

# The Results 
![Pliers GIF](/assets/img/Phone.gif)

The result of this project was a minimal but secure phone holder that was attached to a bike handle bar with a diameter of 25.4 mm. The holder easily rotated between landscape and portrait mode and the TPU band was perfect for securing the phone and allowing it to be removed easily. 

{% include gallery caption="Phone Holder" %}
