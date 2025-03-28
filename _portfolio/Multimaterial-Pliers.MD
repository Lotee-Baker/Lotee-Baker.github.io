---
title: "Multi-Material Pliers"
excerpt: "Print in place multimaterial pliers capable of picking up a resistor"
header:
  image: /assets/img/Pliers.jpg
  teaser: /assets/img/Pliers.jpg
gallery:
  - url: /assets/img/Pliers.jpg
    image_path: /assets/img/Pliers.jpg
    alt: "placeholder image 1"
---

# The Goal 
The goal of this project was to design true print-in-place needle-nose pliers capable of picking up a single resistor at a time. Print-in-place parts are not commonly used in the market today for several reasons, but a true print-in-place design must meet specific criteria: it cannot require supports, and no modifications should be needed after printing. In other words, the pliers should be ready to use immediately after being removed from the print bed.
While websites like Thingiverse feature a "print-in-place" section with designs like the "Flexi Rex" or "Friendly Articulated Slug," these aren't truly print-in-place. Their have weak connections that require breaking post-print to function properly. Similarly, most plier designs available online consist of multiple parts that need to be assembled, which disqualifies them from being true print-in-place parts.
To achieve a genuinely functional print-in-place design, I turned to multi-material 3D printing. One of the most common and effective combinations for this is PLA and TPU. PLA provides the necessary rigidity for the handles and tips, ensuring enough force can be applied without excessive bending. TPU, on the other hand, is perfect for the center joint due to its elasticity. This flexible joint allows the pliers to compress when the handles are squeezed, bringing the tips together to grasp a resistor. By leveraging these two materials, I was able to design a fully functional, print-in-place part that requires no support material and works immediately after printing—no assembly or post-processing needed.

# The Design 
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a41e340cb8bc464afd?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

The pliers consist of five parts: two matching PLA handles, two matching PLA tips, and one TPU center. The total length of the pliers is around 190 mm, with 10 mm-long jaws. When fully relaxed, the jaws remain 10 mm apart—a crucial distance since TPU has a compression limit. The 30 mm x 30 mm TPU center is designed to compress up to half its length (15 mm), providing the necessary gripping action.
A key feature of this design is the TPU center’s hollow "grid" structure, which enables flexibility and allows the pliers to function properly. While the TPU center appears solid in the CAD model, it will be printed with a grid pattern that gives it the ability to compress and spring back. Designing this manually in CAD can be time-consuming, so I took advantage of SuperSlicer’s auto-generated grid infill. By setting the top and bottom layers to zero, I ensured the TPU remained flexible. Additionally, I increased the wall thickness to five layers to guarantee strong, well-formed dovetails for secure connections.
For the PLA handles and tips, I stuck with the slicer's default settings, as they provided the necessary strength and precision. The final result is a fully functional, print-in-place tool that can be printed on a multi-material 3D printer with no supports and is ready for immediate use.

# The Results 
!
This project showcases the potential of multi-material 3D printing in creating real, working print-in-place parts—not just novelty trinkets. If you have access to a multi-material printer and want to try a true print-in-place functional tool, these pliers are a great example of what’s possible!
