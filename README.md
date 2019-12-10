<div class="video-responsive">
<iframe width="800" height="450" src="https://www.youtube.com/embed/Z99n9q5OYKk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

  
I've always enjoyed the aesthetics of pen plotters, both in the way they operate, and their output. And unlike most digital machines that interface with the physical world, they actually get better at the transition point. Laser cutters make a smell, they burn or melt edges and leave behind a kerf. 3D printers are slow, and leave behind layer lines or heaps of PLA spaghetti. But pen plotters have a delightful slow, deliberate movement that is both cleanly digital and unavoidably textured.

I have an old HP 7475A plotter, but I wanted to try making my own. Not least because I've just made a 1-axis CNC machine ([a camera slider](../fab-slider)) so wanted to continue learning by adding another axis. In particular, I learned from the previous project that geting a machine to 90% good enough is easy. The real work is in that last 10%. If I want to create really good plots, I need to make a really good plotter.



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

This version build on what I learned with version 1. Most obviously, it uses a traditional 'cartesian' design, where movement in the y-axis is provided by a motorized arm, while the drawing surface stays still. This has the benefit of much greater accuracy. It also means that you can, in theory, draw on any flat surface. 

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

### Electronics

I'm using an Arduino Uno with a CNC shield and two stepper drivers. I prototyped with the standard (and cheap) A4988 drivers, but switched over to Trinamic drivers which chop much more smoothly down to 1/256 microsteps, resulting in much quieter motion.

You can use pretty much any Trinamic driver board. There is a good comparison here: <https://learn.watterott.com/silentstepstick/comparison/>


### Software

The Arduino is loaded with Grbl firmware, pretty much stock, but I'm using one of the many variants that lets you control a servo for pen up and pen down.

<https://github.com/robottini/grbl-servo>

### Photos and video

There's a short demo on YouTube: <https://youtu.be/Z99n9q5OYKk>  
And lots of photos on Github: <https://github.com/andrewsleigh/plotter/tree/master/photos/v2>




### Workflow

Most of my plots are procedurally generated in Processing or p5. I write sketches that are optimised to create continuous lines and curves: no pixel data or, colours or line styles. So far, I haven't figured out a way to use the 3D renderer in p5, and still be able to export the artwork as an SVG. Either way, I start with vector line art. 

The plotter expects G-Code commands. Typically these are used by CNC machines such as mills, 3D printers and laser cutters. Most of the instructions are shared between machine types except at the business end. The plotter expects pen up and pen down commands to move the pen. (In HPGL, the language used by HP plotters, these are `PU` and `PD`.) Here, we can piggy back on G-Code commands intended to control the power of a laser. So where a laser cutter might start a line by switching the laser on to a certain power, we can use the same command but send it to the servo to move the wiper and drop the pen. This is what the modified Grbl firmware does. 

I use the [J Tech Inkscape Laser Plug-In](https://jtechphotonics.com/?page_id=2012) to generate a G-Code file from the SVG in Inkscape. Currently I can only get this to work in Inkscape 0.9, which is 32 bit, and therefore not compatible with macOS Catalina.

Then I use [CNCJS](https://cnc.js.org) to send commands to the plotter. They even have a half-decent [desktop app](https://github.com/cncjs/cncjs/wiki/Desktop-App). 




### Mechanical parts

I'm using [62oz Nema 17 stepper motors](https://ooznest.co.uk/product/nema17-stepper-motors/) from Ooznest (UK) and a standard SG90 micro servo to lift/drop the pen. 
