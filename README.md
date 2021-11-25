<p>
<div class="video-responsive">
<iframe width="800" height="450" src="https://www.youtube.com/embed/pfx2bN_xx8s" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</p>

* **Update: 2020-03-04. I'm currently on version 3 of the design – scroll down to see the current design and download files**
* **Update: 2021-07-06. I've added a BOM, after many requests!**

## Support my work!

If you like this project or would like to say thanks, you can buy my plotter artwork from https://penuppendown.square.site. I'd really appreciate your support :) 

## Background

I've always enjoyed the aesthetics of pen plotters, both in the way they operate, and their output. And unlike most digital machines that interface with the physical world, they actually get better at the transition point. Laser cutters make a smell, they burn or melt edges and leave behind a kerf. 3D printers are slow, and leave behind layer lines or heaps of PLA spaghetti. But pen plotters have a delightful slow, deliberate movement that is both cleanly digital and unavoidably textured.

I have an old HP 7475A plotter, but I wanted to try making my own. Not least because I've just made a 1-axis CNC machine ([a camera slider](../fab-slider)) so wanted to continue learning by adding another axis. In particular, I learned from the previous project that getting a machine to 90% good enough is easy. The real work is in that last 10%. If I want to create really good plots, I need to make a really good plotter.



## Version 1: Endless Plotter

![](https://github.com/andrewsleigh/plotter/raw/master/photos/v1/IMG_3531.jpg)

I was inspired to start this project when I saw [this plotter featured on Hackaday](https://hackaday.com/2019/08/26/3d-printed-pen-plotter-is-as-big-as-you-need-it-to-be/). As well as being nicely finished, it has a clever design that moves the pen in one axis, and the paper in the other, much like a commercial plotter or inkjet printer.

This has a couple of nice benefits: 
* It has a more compact footprint (when not in use) – it's only as big as its x-axis.
* It can, in theory, plot an endlessly large (in the y-axis) piece of artwork.

I made a version of this plotter, adapting the original 3D files and had some success  with it in practice, but I eventually decided this format was too compromised for me – I couldn't get the paper to feed back and forth reliably. So I switched to a more traditional 'Cartesian' format for version 2, where the y-axis is carried on top of the x-axis, and the plotter sits on top of the paper.

However, I've shared my 3D files here for others to use if interested. Most of the parts have been redesigned from scratch, except for the pen carriage, which is pretty close to the original design by [Ufficio Progetti Perduti](https://www.thingiverse.com/thing:3789969)

* [3D files on Thingiverse](https://www.thingiverse.com/thing:3986756)
* [3D files on Github](https://github.com/andrewsleigh/plotter/tree/master/3d-parts/v1)
* [Photos on Github](https://github.com/andrewsleigh/plotter/tree/master/photos/v1)


## Version 2: Cartesian Plotter

![Plotter v2](https://github.com/andrewsleigh/plotter/raw/master/photos/v2/IMG_6515.jpg)

This version builds on what I learned with version 1. Most obviously, it uses a traditional 'cartesian' design, where movement in the y-axis is provided by a motorized arm, while the drawing surface stays still. This has the benefit of much greater accuracy. It also means that you can, in theory, draw on any flat surface. 


However the drawbacks are that:

1. It needs much more space. With about 50 cm of travel in each axis, it needs a space that big to store, and 1 m x 50 cm to operate.
2. The long arm (with steel rods in my case) is heavy, so it tends to dip towards the end of its reach. This can cause problems getting the right pen height or pressure. To alleviate this, my design has bolt-down points on the x-axis. By bolting this axis to a piece of plywood, the frame is much stiffer. 

Some other features worth noting: 

* I'm using small sections of kite poles to hold the two parts of the pen lifter assembly together. I found 0.1 mm of extra clearance on one part was enough to allow smooth running without wobble.

* In an idea I lifted from Evil Mad Scientist's AxiDraw, I'm using thin strips of flexible polypropylene plastic to support the wires to the servo and y-axis stepper. 

### 3D design

* [3D files on Thingiverse](https://www.thingiverse.com/thing:4037180)
* [3D files on Github](https://github.com/andrewsleigh/plotter/tree/master/3d-parts/v2)
* [Photos on Github](https://github.com/andrewsleigh/plotter/tree/master/photos/v2)

### Photos and video


<p>
<div class="video-responsive">
<iframe width="800" height="450" src="https://www.youtube.com/embed/Z99n9q5OYKk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</p>

There's a short demo on YouTube: <https://youtu.be/Z99n9q5OYKk>  
And lots of photos on Github: <https://github.com/andrewsleigh/plotter/tree/master/photos/v2>



## Version 3: Cartesian Plotter with V-slot axis

![Plotter v3 2060](https://github.com/andrewsleigh/plotter/raw/master/photos/v3/IMG_6608.jpg)

![Plotter v3 2060](https://github.com/andrewsleigh/plotter/raw/master/photos/v3/IMG_6656.jpg)

![Plotter v3 2060](https://github.com/andrewsleigh/plotter/raw/master/photos/v3/IMG_6664.jpg)


Previous designs used 10mm steel rods for the x-axis. These are prone to flexing in the assembly, and the linear bearings are also noisy. So I wanted to switch to a design that used a wheeled gantry sliding on v-slot aluminium extrusion. 

I tried a quick test by hacking a previous project and bolting my existing y-axis to a single axis slide I already had. This worked very well and convinced me it would be worth building a proper x-axis with v-slot.

![Plotter v3 prototype](https://github.com/andrewsleigh/plotter/raw/master/photos/v3/IMG_3819.jpeg)

I already had 2 lengths of 2020 v-slot from my first build, so I initially used these, and made a simple assembly that gained rigidity by bolting these down to a wooden base. 

I ordered a standard v-slot gantry from China, which cost about £10-12, including wheels, bolts and spacers – including eccentric spacers. This allowed me to get a very good fit of the gantry on the x-axis for smooth quiet motion. 

If you don't want to buy an aluminum gantry, could can easily cut one on a laser (as I did for my prototype) or 3D print one from the OpenBuilds design. 

![Plotter v3 2020](https://github.com/andrewsleigh/plotter/raw/master/photos/v3/Cartesian_Plotter_v5_Render_2020-sm.png)

Note, you'll need to tap M5 holes into the ends of the v-slot to attach the two end brackets. The feet are bolted from underneath into the v-slot. 

But then I came into the possession(!) of a 70 cm lngth of 2060 v-slot, so I was able to make a longer, even more stable x-axis. I needed to switch the orientation of the x-axis motor, and raise the axis a little more off the ground to enable th timing belt to go over and under the 2060. I also had to fit a larger 30 tooth pulley. 

But otherwise the principle is the same, I just did a little more work to integrate the electronics and motor. 

![Plotter v3 2060](https://github.com/andrewsleigh/plotter/raw/master/photos/v3/Cartesian_Plotter_v5_Render_2060-sm.png)


### 3D design

* [3D files on Thingiverse](https://www.thingiverse.com/thing:4200863)
* [3D files on Github](https://github.com/andrewsleigh/plotter/tree/master/3d-parts/v3)
* [3D assembly on Fusion online](https://a360.co/2Ily4Dw)
* [Photos on Github](https://github.com/andrewsleigh/plotter/tree/master/photos/v3)



### Improvements over earlier versions

* More stable x-axis (and so less drooping of the pen at it's furthest y-extension)
* Much quieter motion on the x-axis, after swapping out linear bearings fora wheeled gantry
* X-axis can be screwed down to a solid base for greater stability
* Improved brackets for timing belt and linear rods on y-axis so belt can be more easily removed or tightened
* Simplified and more compact pen lifter
* Housing for Arduino and CNC shield can be removed or re-modelled easily (e.g. to fit a smaller Nano-based CNC shield)
* Base has a rebate to fit a 60 cm cutting mat, to allow easier alignment of paper for plotting

## Bill of Materials (BOM)

It’s difficult to give a comprehensive BOM because there is so much flexibility in the design, and so many choices depend on what you have to had. Nevertheless, here is an attempt at a reasonable baseline.

### Motion Control

* Arduino Uno (I’d recommend a genuine Arduino to reduce the risk of EM interference which can play havoc with your servo motor)
* Motor Control Shield
* 2 x Stepper Drivers (A4988-style, but I’d recommend Trinamic drivers for quieter operation)
* 2 x Nema 17 Stepper motors (‘17’ refers to the physical size, you will need to specify the power as well. I used these 7 oz ones from Ooznest, which are fine: https://ooznest.co.uk/product/nema17-stepper-motors/

I’m this configuration the motor control shield is mounted on the Arduino, and the stepper drivers mounted on the shield. You can also get versions that mount a smaller Arduino Nano on to the shield, alongside the drivers, which would make for a more compact design that does the same thing. You would need to adapt the Arduino housing to fit this config.


### X Axis

* Length of 2060 V-Slot aluminium extrusion.
 
(I used a 75 cm length, but anything from 40 cm up is good. Make sure you use V slot and not one of the other profiles of extrusion.An earlier version used two lengths of 2020 extrusion with a 20 mm gap in between. It doesn’t matter, just use what you have. A single piece of 2060 is stiffer, which means less drooping of the pen end and so more reliable plotting, but you could easily make other designs stiffer.)

You will need to tap M5 holes in the ends of the extrusion. 

* 2GT Timing belt (buy a length about 2.5 x the length of your extrusion. (e.g. https://ooznest.co.uk/product/2gt-gates-open-timing-belt-per-metre/)

* 30-tooth 2GT pulley (for 6 mm belt, 5 mm bore) e.g. https://ooznest.co.uk/product/2gt-pulleys/

(This pulley has a large enough diameter to run the belt on either side of the extrusion. If you want to run the belt in a gap inside some extrusion (or you’re using the 2020 design) you’ll need a smaller diameter pulley. You could print one.)

* Idler pulley (of roughly the same diameter as your main pulley) e.g. https://ooznest.co.uk/product/2gt-smooth-idler/. You could also print one.

3D printed parts:

* End bracket for idler pulley
* End bracket for motor
* Shield for motor end (purely cosmetic)
* Box and lid for Arduino
* Feet


### Gantry and Y-axis

* Large v-slot gantry kit (I got mine direct from China, or you can laser cut or 3D print your own)
* 2 x small idler pulleys for y-axis (not the larger Openbuilds pulleys)
* 4 x 8 mm (8UU) linear bearings 
* 2 x 8 mm linear rods

3D printed parts:

* Gantry case

### Pen Lifter

* SG90 Servo motor (e.g. https://thepihut.com/products/towerpro-servo-motor-sg90-hv-continuous-rotation)
* 3 wire jumper extension to extend the wires form the servo back to the motor control board
* 2 x smooth 5 mm diameter rods (I used rods from an old kite. Any smooth, consistent-diameter rods will do, but you will need to adapt the 3D files to fit)

3D printed parts:

* Y axis pen end bracket
* Y axis other end bracket
* Pen lifter
* 3mm bolt cap

### Other Hardware

* Low profile M5 bolts to attach brackets to V-Slot
* Various M3 bolts and nutes (get a selection box)
* Drop-in Tee Nuts for V-Slot e.g. https://ooznest.co.uk/product/drop-in-tee-nuts/
* Some GT2 belt clips, such as cable ties, or these nice removable clips: <http://www.thingiverse.com/thing:2354961>

(In the UK, I'd recommend Ooznest for all the materials you need to buy.)


| Part Number | Qty | Description                                                                                                              | PRICE EA. | Description                                                                                                | Link                                                                                                                                                                                                  |
| ----------- | --- | ------------------------------------------------------------------------------------------------------------------------ | --------- | ---------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| M5 - .80    | 2   | LOCKING NUT                                                                                                              | 0.4       | FOR IDLER PULLEYS                                                                                          |                                                                                                                                                                                                       |
| M3 X 8      | 4   | SCREW                                                                                                                    | 0.27      | WIRE GUIDE- FOR MOUNTING PLASTIC ON Y-AXIS (2)<br>(2) FOR HOLDING ARDUINO TO BOX                           |                                                                                                                                                                                                       |
| M5 X 10     | 3   | SCREW - COUNTERSUNK                                                                                                      | 0.35      | USED 2 FOR LARGE IDLER PULLEY 3D PRINTER PART MOUNTING TO 2060 RAIL                                        |                                                                                                                                                                                                       |
| M3 X 6      | 17  | SCREW                                                                                                                    | 0.23      | USED 12<br>X-AXIS WIRE HOLDER (2)<br>NEMA 17 MOUNTING (8)<br>ARDUINO LID (2)                               |                                                                                                                                                                                                       |
| M3 X 12     | 4   | SCREW - PAN HEAD                                                                                                         | 0.33      | LINEAR ROD CLAMP SCREWS (4)                                                                                |                                                                                                                                                                                                       |
| M3 - .5     | 14  | NUT                                                                                                                      | 0.13      | USED 12<br>LINEAR ROD CLAMP (4)<br>WIRE GUIDE (4)<br>X-AXIS WIRE HOLDER (2)<br>MOUNTING ARDUINO TO BOX (2) |                                                                                                                                                                                                       |
| M3 X 30     | 1   | SCREW - SOCKET HEAD                                                                                                      | 0.85      | PEN HOLDER                                                                                                 |                                                                                                                                                                                                       |
| M5          | 10  | WASHERS                                                                                                                  | 0.14      | USED 8 FOR IDLER PULLEY                                                                                    |                                                                                                                                                                                                       |
| M5 X 10     | 4   | SCREW - PAN HEAD                                                                                                         | 0.35      | 2060 VSLOT BASES                                                                                           |                                                                                                                                                                                                       |
| M5 X 8      | 2   | SCREW - PAN HEAD                                                                                                         | 0.2       | USED 2 FOR MOUNTING STEPPER MOTOR TO 2060 RAIL (ON END WITH ARDUINO)                                       |                                                                                                                                                                                                       |
| M5 X 35     | 4   | SCREW - PAN HEAD                                                                                                         | 0.55      | FOR MOUNTING STEPPER MOTOR ASSEMBLY TO GANTRY PLATE, HAD TO CUT DOWN FOR CLEARANCE                         |                                                                                                                                                                                                       |
| M5 - .80    | 8   | NUT                                                                                                                      | 0.16      | STEPPER MOTOR ASSEMBLY TO GANTRY PLATE (4)                                                                 |                                                                                                                                                                                                       |
| M5 X 25     | 3   | SCREW - COUNTERSUNK                                                                                                      | 0.55      | USED 2 FOR IDLER PULLEYS                                                                                   |                                                                                                                                                                                                       |
| SG-90       | 1   | SERVO                                                                                                                    | 2.75      | PIN LIFTER (4 PACK, $10.99)                                                                                | [https://www.amazon.com/gp/product/B07MLR1498/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s03?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B07MLR1498/ref=ppx_yo_dt_b_asin_title_o05_s03?ie=UTF8&psc=1) |
|             | 2   | 7 CM X 5MM CARBON RODS                                                                                                   | 12.49     | PEN LIFTER (FOR 5 PCS, CUT DOWN TO 7 CM)                                                                   | [https://www.amazon.com/gp/product/B07P81VMPF/ref=ppx\_yo\_dt\_b\_asin\_title\_o04\_s00?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B07P81VMPF/ref=ppx_yo_dt_b_asin_title_o04_s00?ie=UTF8&psc=1) |
|             | 2   | LINEAR RODS 8MM X 500MM                                                                                                  | 9.95      | Y AXIS (2 PACK)                                                                                            | [https://www.amazon.com/gp/product/B07DPFH7HL/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s02?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B07DPFH7HL/ref=ppx_yo_dt_b_asin_title_o05_s02?ie=UTF8&psc=1) |
|             | 66  | GT2 TIMING BELT ~ 66 INCHES                                                                                              | 11.99     | CAME WITH 196 INCHES                                                                                       | [https://www.amazon.com/gp/product/B0776KXY8G/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s01?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B0776KXY8G/ref=ppx_yo_dt_b_asin_title_o05_s01?ie=UTF8&psc=1) |
|             | 1   | 20 TOOTH, 5MM TIMING PULLEY ^ INCLUDED WITH BELT                                                                         |           | CAME IN 8 PACK                                                                                             |                                                                                                                                                                                                       |
|             | 4   | LINEAR BEARINGS, 8 X 15 X 24MM                                                                                           | 0.84      | CAME IN 12 PACK                                                                                            | [https://www.amazon.com/gp/product/B08GSK5ZQB/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s03?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B08GSK5ZQB/ref=ppx_yo_dt_b_asin_title_o05_s03?ie=UTF8&psc=1) |
|             | 2   | 5MM IDLER PULLEYS FOR 6MM TIMING BELT<br>INNER DIAMETER = 12 MM<br>FLANGE DIAMETER = 18 MM<br>BORE = 5MM<br>WIDTH = ~9MM | 1.6       | (CAME IN PACK OF 5)                                                                                        | [https://www.amazon.com/gp/product/B01H3F8LUU/ref=ppx\_od\_dt\_b\_asin\_title\_s03?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B01H3F8LUU/ref=ppx_od_dt_b_asin_title_s03?ie=UTF8&psc=1)          |
|             | 1   | GANTRY PLATE KIT                                                                                                         | 39.59     |                                                                                                            | [https://www.amazon.com/gp/product/B08LDM3QFD/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s01?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B08LDM3QFD/ref=ppx_yo_dt_b_asin_title_o05_s01?ie=UTF8&psc=1) |
|             | 1   | 2060 LINEAR RAIL - 500MM                                                                                                 | 21.99     |                                                                                                            | [https://www.amazon.com/gp/product/B08GCQXDBR/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s00?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B08GCQXDBR/ref=ppx_yo_dt_b_asin_title_o05_s00?ie=UTF8&psc=1) |
|             | 2   | NEMA 17 42MM X 40MM, 0.46 NM TORQUE                                                                                      | 17.59     |                                                                                                            | [https://www.amazon.com/gp/product/B06XSYP24P/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s01?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B06XSYP24P/ref=ppx_yo_dt_b_asin_title_o05_s01?ie=UTF8&psc=1) |
|             | 6   | SMALL WOOD SCREWS FOR MOUNTING ENTIRE ASSEMBLY TO PIECE OF WOOD                                                          |           |                                                                                                            |                                                                                                                                                                                                       |
|             | 2   | SMALL SCREWS FOR MOUNTING ARDUINO LID                                                                                    |           |                                                                                                            |                                                                                                                                                                                                       |
|             | 4   | M5 T-SLOT NUTS                                                                                                           | 0.08      |                                                                                                            | [https://www.amazon.com/gp/product/B07NZKK1PM/ref=ppx\_yo\_dt\_b\_asin\_title\_o02\_s00?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B07NZKK1PM/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&psc=1) |
|             | 1   | ARDUINO UNO CNC KIT (off brand)                                                                                          | 17.99     |                                                                                                            | [https://www.amazon.com/gp/product/B06XHKSVTG/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s03?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B06XHKSVTG/ref=ppx_yo_dt_b_asin_title_o05_s03?ie=UTF8&psc=1) |
|             | 1   | CNC SHIELD EXPANSION BOARD                                                                                               |           | CAME WITH ARDUINO KIT                                                                                      |                                                                                                                                                                                                       |
|             | 2   | A4988 DRIVERS                                                                                                            |           | CAME WITH ARDUINO KIT - JUMPERS INCLUDED                                                                   |                                                                                                                                                                                                       |
|             | 1   | 30 TOOTH 5MM BORE TIMING PULLEY                                                                                          | 3.99      | CAME IN PACK OF 2                                                                                          | [https://www.amazon.com/gp/product/B089LW6XTV/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s03?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B089LW6XTV/ref=ppx_yo_dt_b_asin_title_o05_s03?ie=UTF8&psc=1) |
|             | 1   | PLASTIC FOR SALE SIGN USED FOR MAKING WIRE HOLDERS                                                                       | 4.99      |                                                                                                            |                                                                                                                                                                                                       |
|             | 1   | SMOOTH IDLER PULLEY KIT                                                                                                  | 5.99      |                                                                                                            | [https://openbuildspartstore.com/smooth-idler-pulley-kit/](https://openbuildspartstore.com/smooth-idler-pulley-kit/)                                                                                  |



| **Part Number** | **Qty** | **Description**                                                                                                  | **PRICE EA.** | **Description**                                                                                    | **Link**                                                                                                                                                                                              |
| --------------- | ------- | ---------------------------------------------------------------------------------------------------------------- | ------------- | -------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| M5 - .80        | 2       | LOCKING NUT                                                                                                      | 0.4           | FOR IDLER PULLEYS                                                                                  |                                                                                                                                                                                                       |
| M3 X 8          | 4       | SCREW                                                                                                            | 0.27          | WIRE GUIDE- FOR MOUNTING PLASTIC ON Y-AXIS (2)

(2) FOR HOLDING ARDUINO TO BOX                     |                                                                                                                                                                                                       |
| M5 X 10         | 3       | SCREW - COUNTERSUNK                                                                                              | 0.35          | USED 2 FOR LARGE IDLER PULLEY 3D PRINTER PART MOUNTING TO 2060 RAIL                                |                                                                                                                                                                                                       |
| M3 X 6          | 17      | SCREW                                                                                                            | 0.23          | USED 12

X-AXIS WIRE HOLDER (2)

NEMA 17 MOUNTING (8)

ARDUINO LID (2)                             |                                                                                                                                                                                                       |
| M3 X 12         | 4       | SCREW - PAN HEAD                                                                                                 | 0.33          | LINEAR ROD CLAMP SCREWS (4)                                                                        |                                                                                                                                                                                                       |
| M3 - .5         | 14      | NUT                                                                                                              | 0.13          | USED 12

LINEAR ROD CLAMP (4)

WIRE GUIDE (4)

X-AXIS WIRE HOLDER (2)

MOUNTING ARDUINO TO BOX (2) |                                                                                                                                                                                                       |
| M3 X 30         | 1       | SCREW - SOCKET HEAD                                                                                              | 0.85          | PEN HOLDER                                                                                         |                                                                                                                                                                                                       |
| M5              | 10      | WASHERS                                                                                                          | 0.14          | USED 8 FOR IDLER PULLEY                                                                            |                                                                                                                                                                                                       |
| M5 X 10         | 4       | SCREW - PAN HEAD                                                                                                 | 0.35          | 2060 VSLOT BASES                                                                                   |                                                                                                                                                                                                       |
| M5 X 8          | 2       | SCREW - PAN HEAD                                                                                                 | 0.2           | USED 2 FOR MOUNTING STEPPER MOTOR TO 2060 RAIL (ON END WITH ARDUINO)                               |                                                                                                                                                                                                       |
| M5 X 35         | 4       | SCREW - PAN HEAD                                                                                                 | 0.55          | FOR MOUNTING STEPPER MOTOR ASSEMBLY TO GANTRY PLATE, HAD TO CUT DOWN FOR CLEARANCE                 |                                                                                                                                                                                                       |
| M5 - .80        | 8       | NUT                                                                                                              | 0.16          | STEPPER MOTOR ASSEMBLY TO GANTRY PLATE (4)                                                         |                                                                                                                                                                                                       |
| M5 X 25         | 3       | SCREW - COUNTERSUNK                                                                                              | 0.55          | USED 2 FOR IDLER PULLEYS                                                                           |                                                                                                                                                                                                       |
| SG-90           | 1       | SERVO                                                                                                            | 2.75          | PIN LIFTER (4 PACK, $10.99)                                                                        | [https://www.amazon.com/gp/product/B07MLR1498/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s03?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B07MLR1498/ref=ppx_yo_dt_b_asin_title_o05_s03?ie=UTF8&psc=1) |
|                 | 2       | 7 CM X 5MM CARBON RODS                                                                                           | 12.49         | PEN LIFTER (FOR 5 PCS, CUT DOWN TO 7 CM)                                                           | [https://www.amazon.com/gp/product/B07P81VMPF/ref=ppx\_yo\_dt\_b\_asin\_title\_o04\_s00?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B07P81VMPF/ref=ppx_yo_dt_b_asin_title_o04_s00?ie=UTF8&psc=1) |
|                 | 2       | LINEAR RODS 8MM X 500MM                                                                                          | 9.95          | Y AXIS (2 PACK)                                                                                    | [https://www.amazon.com/gp/product/B07DPFH7HL/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s02?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B07DPFH7HL/ref=ppx_yo_dt_b_asin_title_o05_s02?ie=UTF8&psc=1) |
|                 | 66      | GT2 TIMING BELT ~ 66 INCHES                                                                                      | 11.99         | CAME WITH 196 INCHES                                                                               | [https://www.amazon.com/gp/product/B0776KXY8G/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s01?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B0776KXY8G/ref=ppx_yo_dt_b_asin_title_o05_s01?ie=UTF8&psc=1) |
|                 | 1       | 20 TOOTH, 5MM TIMING PULLEY ^ INCLUDED WITH BELT                                                                 |               | CAME IN 8 PACK                                                                                     |                                                                                                                                                                                                       |
|                 | 4       | LINEAR BEARINGS, 8 X 15 X 24MM                                                                                   | 0.84          | CAME IN 12 PACK                                                                                    | [https://www.amazon.com/gp/product/B08GSK5ZQB/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s03?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B08GSK5ZQB/ref=ppx_yo_dt_b_asin_title_o05_s03?ie=UTF8&psc=1) |
|                 | 2       | 5MM IDLER PULLEYS FOR 6MM TIMING BELT

INNER DIAMETER = 12 MM

FLANGE DIAMETER = 18 MM

BORE = 5MM

WIDTH = ~9MM | 1.6           | (CAME IN PACK OF 5)                                                                                | [https://www.amazon.com/gp/product/B01H3F8LUU/ref=ppx\_od\_dt\_b\_asin\_title\_s03?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B01H3F8LUU/ref=ppx_od_dt_b_asin_title_s03?ie=UTF8&psc=1)          |
|                 | 1       | GANTRY PLATE KIT                                                                                                 | 39.59         |                                                                                                    | [https://www.amazon.com/gp/product/B08LDM3QFD/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s01?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B08LDM3QFD/ref=ppx_yo_dt_b_asin_title_o05_s01?ie=UTF8&psc=1) |
|                 | 1       | 2060 LINEAR RAIL - 500MM                                                                                         | 21.99         |                                                                                                    | [https://www.amazon.com/gp/product/B08GCQXDBR/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s00?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B08GCQXDBR/ref=ppx_yo_dt_b_asin_title_o05_s00?ie=UTF8&psc=1) |
|                 | 2       | NEMA 17 42MM X 40MM, 0.46 NM TORQUE                                                                              | 17.59         |                                                                                                    | [https://www.amazon.com/gp/product/B06XSYP24P/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s01?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B06XSYP24P/ref=ppx_yo_dt_b_asin_title_o05_s01?ie=UTF8&psc=1) |
|                 | 6       | SMALL WOOD SCREWS FOR MOUNTING ENTIRE ASSEMBLY TO PIECE OF WOOD                                                  |               |                                                                                                    |                                                                                                                                                                                                       |
|                 | 2       | SMALL SCREWS FOR MOUNTING ARDUINO LID                                                                            |               |                                                                                                    |                                                                                                                                                                                                       |
|                 | 4       | M5 T-SLOT NUTS                                                                                                   | 0.08          |                                                                                                    | [https://www.amazon.com/gp/product/B07NZKK1PM/ref=ppx\_yo\_dt\_b\_asin\_title\_o02\_s00?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B07NZKK1PM/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&psc=1) |
|                 | 1       | ARDUINO UNO CNC KIT (off brand)                                                                                  | 17.99         |                                                                                                    | [https://www.amazon.com/gp/product/B06XHKSVTG/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s03?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B06XHKSVTG/ref=ppx_yo_dt_b_asin_title_o05_s03?ie=UTF8&psc=1) |
|                 | 1       | CNC SHIELD EXPANSION BOARD                                                                                       |               | CAME WITH ARDUINO KIT                                                                              |                                                                                                                                                                                                       |
|                 | 2       | A4988 DRIVERS                                                                                                    |               | CAME WITH ARDUINO KIT - JUMPERS INCLUDED                                                           |                                                                                                                                                                                                       |
|                 | 1       | 30 TOOTH 5MM BORE TIMING PULLEY                                                                                  | 3.99          | CAME IN PACK OF 2                                                                                  | [https://www.amazon.com/gp/product/B089LW6XTV/ref=ppx\_yo\_dt\_b\_asin\_title\_o05\_s03?ie=UTF8&psc=1](https://www.amazon.com/gp/product/B089LW6XTV/ref=ppx_yo_dt_b_asin_title_o05_s03?ie=UTF8&psc=1) |
|                 | 1       | PLASTIC FOR SALE SIGN USED FOR MAKING WIRE HOLDERS                                                               | 4.99          |                                                                                                    |                                                                                                                                                                                                       |
|                 | 1       | SMOOTH IDLER PULLEY KIT                                                                                          | 5.99          |                                                                                                    | [https://openbuildspartstore.com/smooth-idler-pulley-kit/](https://openbuildspartstore.com/smooth-idler-pulley-kit/)                                                                                  |


## Electronics

I'm using an Arduino Uno with a CNC shield and two stepper drivers. I prototyped with the standard (and cheap) A4988 drivers, but switched over to Trinamic drivers which chop much more smoothly down to 1/256 microsteps, resulting in much quieter motion.

You can use pretty much any Trinamic driver board. There is a good comparison here: <https://learn.watterott.com/silentstepstick/comparison/>

## Power

The plotter requires 12V power, and your supply should be good enough to supply the current your steppers demand. (Mine is a 1.5A 12V supply)

You can plug this straight into the 12V barrel jack on the Arduino, which will give 5V reulated power to the Arduino, and 12V onto the CNC shield. 

**BUT YOU MUST HACK YOUR CNC SHIELD FIRST:** You need to wire the VIN pin on the CNC shield to the positive power terminal. Like this: http://3dpburner.blogspot.com/p/bluetooth-connection.html?m=1


### Software and Workflow

The plotter expects G-Code commands. Typically these are used by CNC machines such as mills, 3D printers and laser cutters. Most of the instructions are shared between machine types except at the business end. The plotter expects pen up and pen down commands to move the pen. (In HPGL, the language used by HP plotters, these are `PU` and `PD`.) Here, we can piggy back on G-Code commands intended to control the power of a laser. So where a laser cutter might start a line by switching the laser on to a certain power, we can use the same command but send it to the servo to move the wiper and drop the pen. This is what the modified Grbl firmware does. 

The chain of tools/processes is basically:

Create artwork > export as vectors (SVG, PDF, etc) > Create GCODE from vector file > Stream GCODE to Arduino > Use Grbl firmware on Arduino to control motors

### Art

Most of my plots are procedurally generated in Processing or p5. I write sketches that are optimised to create continuous lines and curves: no pixel data or, colours or line styles. So far, I haven't figured out a way to use the 3D renderer in p5, and still be able to export the artwork as an SVG. Either way, I start with vector line art.

I also use Blender, which has loads of options for exporting 2D vector data from 3D models.

### Create GCODE

After too much time wasted with Inkscape plug-ins I have switched to [Lightburn](https://lightburnsoftware.com) to create GCode. I find it works well with PDF files.


### Stream GCODE

There are numerous GRBL interfaces available, and I've always had good results with [CNCJS](https://cnc.js.org), which is bundled up as a webview inside a Mac app. However, that can hog the machine CPU, and also means your laptop is tethered to the plotter. So now I [run CNCJS on a local Node server on a Raspberry Pi](https://cnc.js.org/docs/rpi-setup-guide/) (Model 4, 2GBRAM) connected by USB cable to the plotter. It auto-runs as soon as the Pi boots, and I can access it through a web browser to start a job or check in later. I can always switch to CNCJS running on the laptop by unplugging the Pi.

The plotter expects a stream of GCode commands to control the motors. There are many ways you can chain together software to get to this stage. Working backwards from the plotter:

### Motor control

The Arduino is loaded with Grbl firmware, pretty much stock, but I'm using one of the many variants that lets you control a servo for pen up and pen down.

<https://github.com/robottini/grbl-servo>



