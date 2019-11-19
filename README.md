# DIY Pen Plotter


## Introduction


I've always enjoyed the aesthetics of pen plotters, both in the way they operate, and their output. And unlike most digital machines that interface with the physical world, they actually get better at the transition point. Laser cutters make a smell, they burn or melt edges and leave behind a kerf. 3D printers are slow, and leave behind layer lines or heaps of PLA spaghetti. But pen plotters have a delightful slow, deliberate movement that is both cleanly digital and unavoidably textured.

I have an old HP 7475A plotter, but I wanted to try making my own. Not least because I've just made a 1-axis CNC machine (a camera slider) so wanted to continue learning by adding another axis. In particular, I learned from the previous project that geting a machine to 90% good enough is easy. The real work is in that last 10%. If I want to create really good plots, I need to make a really good plotter.



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


#More details and files coming soon!#

3D design


### Electronics

I'm using an Arduino Uno with a CNC shield and two stepper drivers. I prototyped with the standard (and cheap) A4988 drivers, but switched over to Trinamic drivers which chop much more smoothly down to 1/256 microsteps, resulting in much quieter motion.

You can use pretty much any Trinamic driver board. There is a good comparison here: <https://learn.watterott.com/silentstepstick/comparison/>


### Software

The Arduino is loaded with Grbl firmware, pretty much stock, but I'm using one of the many variants that lets you control a servo for pen up and pen down.

<https://github.com/robottini/grbl-servo>

### Workflow

#Coming soon ...#


### Mechanical parts

I'm using [62oz Nema 17 stepper motors](https://ooznest.co.uk/product/nema17-stepper-motors/) from Ooznest (UK) and a standard SG90 micro servo to lift/drop the pen. 
