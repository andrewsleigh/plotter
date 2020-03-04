<p>
<div class="video-responsive">
<iframe width="800" height="450" src="https://www.youtube.com/embed/Z99n9q5OYKk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</p>

**Update: 2020-03-04. I'm currently on version 3 of the design – scroll down to see the current design and download files.**
  
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

* In an idea I lifted from Evil Mad Scientist's AxiDraw, I'm using thin strips of flexible plastic (polypropylene I think) to support the wires to the servo and y-axis stepper. 

### 3D design

* [3D files on Thingiverse](https://www.thingiverse.com/thing:4037180)
* [3D files on Github](https://github.com/andrewsleigh/plotter/tree/master/3d-parts/v2)
* [Photos on Github](https://github.com/andrewsleigh/plotter/tree/master/photos/v2)


## Version 3: Cartesian Plotter with V-slot axis

Note: I'm currently working on photos for this version - for now, here are some renders.

![Plotter v3 2060](https://github.com/andrewsleigh/plotter/raw/master/photos/v3/Cartesian_Plotter_v5_Render_2060-sm.png)

Previous designs used 10mm steel rods for the x-axis. These are prone to flexing in the assembly, and the linear bearings are also noisy. So I wanted to switch to a design that used a wheeled gantry sliding on v-slot aluminium extrusion. 

I tried a quick test by hacking a previous project and bolting my existing y-axis to a single axis slide I already had. This worked very well and convinced me it would be worth building a proper x-axis with v-slot.

![Plotter v3 prototype](https://github.com/andrewsleigh/plotter/raw/master/photos/v3/IMG_3819.jpeg)

I already had 2 lengths of 2020 v-slot from my first build, so I initially used these, and made a simple assembly that gained rigidity by bolting these down to a wooden base. 

I ordered a standard v-slot gantry from China, which cost about £10-12, including wheels, bolts and spacers – including eccentric spacers. This allowed me to get a very good fit of the gantry on the x-axis for smooth quiet motion. 

If you don't want to buy an aluminum ganry, could can easily cut one on a laser (as I did for my prototype) or 3D print one from the OpenBuilds design. 

![Plotter v3 2020](https://github.com/andrewsleigh/plotter/raw/master/photos/v3/Cartesian_Plotter_v5_Render_2020-sm.png)

Note, you'll need to tap M5 holes into the ends of the v-slot to attach the two end brackets. The feet are bolted frmo underneath into the v-slot. 

But then I came into the possession(!) of a 70 cm lngth of 2060 v-slot, so I was able to make a longer, even more stable x-axis. I needed to switch the orientation of the x-axis motor, and raise the axis a little more off the ground to enable th timing belt to go over and under the 2060. I also had to fit a larger 30 tooth pulley. 

But otherwise the principle is the same, I just did a little more work to integrate the electronics and motor. 

![Plotter v3 2060](https://github.com/andrewsleigh/plotter/raw/master/photos/v3/Cartesian_Plotter_v5_Render_2060-sm.png)


### 3D design

<!-- * [3D files on Thingiverse](https://www.thingiverse.com/thing:4037180) -->
* [3D files on Github](https://github.com/andrewsleigh/plotter/tree/master/3d-parts/v3)
* [3D assembly on Fusion online](https://a360.co/2Ily4Dw)
* [Photos on Github]<!-- (https://github.com/andrewsleigh/plotter/tree/master/photos/v2) --> Coming soon



### Improvements over earlier versions

* More stable x-axis (and so less drooping of the pen at it's furthest y-extension)
* X-axis can be screwed down to a solid base for greater stability
* Improved brackets for timing belt and linear rods on y-axis so belt can be more easily removed or tightened
* Simplified and more compact pen lifter
* Housing for Arduino and CNC shield can be removed or re-modelled easily (e.g. to fit a smaller Nano-based CNC shield)

### Other parts you'll need

* 2 NEMA 17 motors
* 2 GT2 timing belts
* 30 or 40 tooth pulley for x-axis timing belt
* 20 tooth pulley for x-axis timing belt
* Large idley pulley for x-axis timing belt
* 2 small idler pulleys for y-axis
* 5 mm rods for pen lifter
* Plenty of M5 and M3 hardware!
* Large v-slot gantry kit
* Servo motor



## Electronics

I'm using an Arduino Uno with a CNC shield and two stepper drivers. I prototyped with the standard (and cheap) A4988 drivers, but switched over to Trinamic drivers which chop much more smoothly down to 1/256 microsteps, resulting in much quieter motion.

You can use pretty much any Trinamic driver board. There is a good comparison here: <https://learn.watterott.com/silentstepstick/comparison/>


### Software

The Arduino is loaded with Grbl firmware, pretty much stock, but I'm using one of the many variants that lets you control a servo for pen up and pen down.

<https://github.com/robottini/grbl-servo>

### CAM

There are nmerous GRBL interfaces availabl, and I've always had good results with [CNCJS](https://cnc.js.org), which is bundled up as a webview inside a Mac app. However, that can hog the machine CPU, and also means your laptop is tethered to the plotter. So now I [run CNCJS on a local Node server on a Raspberry Pi](https://cnc.js.org/docs/rpi-setup-guide/) (Model 4, 2GBRAM) connected by USB cable to the plotter. It auto-runs as soon as the Pi boots, and I can acess it through a web browser to start a job or check in later. I can always switch to CNCJS running on the laptop by unplugging the Pi.

### Photos and video

There's a short demo on YouTube: <https://youtu.be/Z99n9q5OYKk>  
And lots of photos on Github: <https://github.com/andrewsleigh/plotter/tree/master/photos/v2>




### Workflow

Most of my plots are procedurally generated in Processing or p5. I write sketches that are optimised to create continuous lines and curves: no pixel data or, colours or line styles. So far, I haven't figured out a way to use the 3D renderer in p5, and still be able to export the artwork as an SVG. Either way, I start with vector line art. 

The plotter expects G-Code commands. Typically these are used by CNC machines such as mills, 3D printers and laser cutters. Most of the instructions are shared between machine types except at the business end. The plotter expects pen up and pen down commands to move the pen. (In HPGL, the language used by HP plotters, these are `PU` and `PD`.) Here, we can piggy back on G-Code commands intended to control the power of a laser. So where a laser cutter might start a line by switching the laser on to a certain power, we can use the same command but send it to the servo to move the wiper and drop the pen. This is what the modified Grbl firmware does. 

I use the [J Tech Inkscape Laser Plug-In](https://jtechphotonics.com/?page_id=2012) to generate a G-Code file from the SVG in Inkscape. Currently I can only get this to work in Inkscape 0.9, which is 32 bit, and therefore not compatible with macOS Catalina.

Then I use [CNCJS](https://cnc.js.org) to send commands to the plotter. They even have a half-decent [desktop app](https://github.com/cncjs/cncjs/wiki/Desktop-App). 




### Mechanical parts and materials

I'm using [62oz Nema 17 stepper motors](https://ooznest.co.uk/product/nema17-stepper-motors/) from Ooznest (UK) and a standard SG90 micro servo to lift/drop the pen. The rods are 8 mm and 10 mm steel linear rods, also from Ooznest, the pen lifter rods are cut from kite poles, and the cable supports are cut by hand from polypropylene sheet. 3D parts are all printed in PLA.


### Improvements

I've got some ideas about improving on this design, mostly to increase rigidity. ~~First on the list is to experiment with a v-slot and gantry assembly for the x-axis.~~ (Fixed n version 3) And although I'm quite happy with the product design on this version, I'd still like to make it more well-integrated; perhaps find a way to get the motors out of sight.


