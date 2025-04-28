---
title: "Fungal Bookshelf"
excerpt: "Fungal Bookshelf Created With Generative Design"
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
# The Idea
My goal for this generative design part was to take advantage of the asymmetric, unconstrained, almost biological look of generative design and make a fungal-inspired bookshelf. The reason I chose a bookshelf for my project is that I have always had a love for books and, over the years, have amassed a collection that I do not have enough storage for. I could design this shelf with a more classical approach. Classic design in Fusion 360 is very helpful when designing everyday parts. With a multitude of different tools like sketch, extrude, fillet, etc., you can create things like everyday knick-knacks to useful components like a phone holder, which is also featured in my portfolio. This is amazing but also has some limitations. Because everything should be constrained in classic Fusion design so that the dimensions of the part are locked in place, classic Fusion design lends itself to simple, sharp geometries like rectangles, triangles, and circles. There are tools like spline that can create more flowing shapes and designs, but it is very hard to constrain and can, at times, be unruly and frustrating. Another limitation of classic Fusion design is that it is hard to understand how your part is going to react under certain forces, and this can lead to designing heavier, more massive parts than needed. Though it is not bad to have an extra strong part, this can be costly and time-consuming, as most additive manufacturing processes are bottlenecked by the volume of the parts they are printing. Also, with Nylon 12 for powder printing costing more than 100 dollars per kilogram, it can be very cost-effective to reduce the amount of material that your part uses. This is where generative design shines.

# Generative Design
Generative design picks up where classic Fusion 360 design fails. Instead of sharp basic shapes in your parts, generative design creates smooth, winding, asymmetric creations that would be extremely challenging to constrain and design from scratch. The other aspect that is truly unique to generative design is that you can specifically tell it to prioritize minimizing mass while maintaining enough strength to reliably perform its designated purpose. The goal of my design was to truly test and understand the limits of generative design in three ways. First, to test its ability to design a part that can reliably withstand predefined forces and strains. So, I set a clear function for the bookshelf: I want it to hold my favorite series, which is the Throne of Glass series by Sarah J. Maas. This is an 8-book series, so the shelf must be capable of displaying 8 books reliably. I also wanted to test the limits of the creativity and problem-solving of generative design by giving it multiple obstacle geometries to weave around while creating the supports for the shelf. I did this by leaning into the semi-natural aesthetic that generative design has and made my obstacle mushrooms—multiple mushrooms on the base plate. The third way I wanted to test generative design was its ability to minimize mass and size while still producing a reliable part compared to other bookshelf design approaches. I did this by constraining its size to a 100 mm x 100 mm x 86.36 mm volume and selecting the minimize mass option in the design objective. With these goals defined, I could begin to create my bookshelf.

So, how does generative design work? Generative design needs three main constraints to create a part: preserve geometry, obstacle geometry, and applied loads. The application includes and connects all the preserve geometries together and avoids the obstacle geometries, all while calculating the strength and capabilities of those connections based on the applied loads and constraints that you define.

## Preserve and Obstacle Geometry
I created 12 preserve geometries for this bookshelf. One being the base of the shelf with 6 mushroom clusters, and the others are 11 circles 80 mm above the base plate of varying sizes to encourage an asymmetric and interesting generative design. I then created 9 obstacle geometries. Two of them were a plate above and below the preserve geometries to ensure that the top and the bottom were flat, even surfaces. Another obstacle geometry was a 100 x 100 "fence" around the bookshelf to constrain the generative design to that 100 x 100 x 86.36 mm volume. The other six obstacle geometries were 1 mm thick cylinders surrounding the mushrooms so that the generative design wouldn’t obscure or cover the mushrooms and instead would have to wind around them.

## Applied Loads and Constraints
After both the preserve and obstacle geometries were created, I then started to design the applied loads and constraints. I first created a fixed constraint on the bottom face of the base plate. This gives Fusion the information that the base plate will not be bending or moving in any way. This basically defines the base plate as a static object and allows Fusion to make its calculations with that information in mind. I then moved on to defining the loads. I created four load cases.

For the first load case, I only accounted for the main goal, which is reliably holding 8 books. Fusion automatically applies the force of gravity as an applied load in the generative design workspace. The next applied load is the weight of the 8-book series. Setting the assumption that the average weight of a book is 1 kg, the shelf needs to withstand 8 kg of weight, which is 78.5 N of force with gravitational acceleration being 9.81 m/s². I defined this 78.5 N of force by breaking it up and applying 11 compression forces normal to the surfaces of the circles, proportional to their area. The next applied load I defined was a moment on the largest center circle to account for any torque created by off-center book placement. If 0.25 kg of the book's weight is offset by 0.5 mm, the moment created would be 1.22 N mm, which I rounded to 1.5 N mm. I applied this moment in two different directions and oriented them 90 degrees apart to hopefully cover all the possible moments that could be created by off-center book stacking.

For the second and third load cases, I accounted for any shear force that could be created by the bookshelf being bumped from the side. This is very important to account for because I have a cat who likes to rub her head against all the objects in my dorm. I kept all the vertical forces of gravity and the weight of the 8 books from the last load case but I also added four 15 N loads on the 4 largest circles, excluding the center circle. All of these loads were horizontal and in different directions 90 degrees apart. The third load case had two of the horizontal forces opposing each other and the fourth had the other two forces opposing each other.

My last load case was to account for an extreme case. I noticed that one of my corner support circles was particularly small and isolated compared to the rest. So I wanted to create a load case that accounted for potential stresses on that weak spot in that corner of the bookcase. I did this by applying a moment of 1 N mm on that isolated circle to force the generative design to give that circle more support. This load case also had all of the compression forces from the weight of the 8 books and the force of gravity.

insert table 

# Solving the Study and Printing
In generative design you can also set the manufacturing method, safety factor, and material. I set the manufacturing method to unrestricted because I planned to SLS powder print this bookshelf. SLS is perfect for this application because it prints without supports, allowing for more complex geometries. The powder in the printer is Nylon 12 (with the Formlabs Fuse 1 3D Printer), so that is what I set the material to. I then set the safety factor to 1 because there is very little danger if the shelf fails and I really wanted to focus on minimizing mass. With everything now prepared for my generative design, I prompted Fusion to solve and waited for the results.

# Results
The study resulted in one converged shelf with an estimated mass of 0.12 kg and an estimated volume of 118,281 mm³. I then took this design and converted it to a mesh. After converting it to a mesh, I repaired it and reduced it so that it could be converted to a body and exported as an STL file. I then printed the bookshelf on an SLS printer in Nylon 12, cleaned the part, and tested it. The shelf successfully held 8 books.

I do enjoy the look of the bookshelf, but I do think there were some flaws in the generative design. It did not follow all of the obstacle geometries completely, covering most of the small mushroom clusters on the base plate. It also failed to directly convert to a body, which only gave me the option to convert it to a mesh. This is okay because I can then reduce the mesh and create a body from there, but it prevents me from using tools like smooth where I could’ve cleaned up some of the creases and holes in the shelf. Overall, I still think that generative design can be extremely useful in the prototyping phase of applications where you need to make something both lightweight and strong enough to serve a very specific purpose. I believe that it can give a lot of insight into where the most force will be applied and where your part needs to be the strongest, which can give you a good jumping-off point when trying to design a lightweight part. This can be very useful for the sports car industry as engineers are always trying to decrease the weight of their cars, which is an uphill battle because most cars undergo extremely large forces and need to be very robust.

If I were to do this project again, I would test my first bookshelf and see at what forces it fails. If it withstands significantly more force than it needs to—aka it holds 20 books—I would decrease the forces and moments applied to it to further decrease its mass. I would also increase the wall thickness of the cylindrical obstacle geometries surrounding the mushrooms. I only made the cylinders 1 mm thick, and that may have been why the generative design crossed so many of the obstacle boundaries. Perhaps if I increased the thickness of the obstacles, Fusion would have had an easier time avoiding them.

Overall, I am still very happy with this bookshelf as I really believe it blends well with its fungal inspiration, and I am excited to have a new and unique shelf to display my favorite series.


