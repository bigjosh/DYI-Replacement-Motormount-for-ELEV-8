# DYI-Replacement-Motormount-for-ELEV-8
Files for making your own [replacement motor mounts for the Parallax ELEV-8 drone](https://www.parallax.com/product/721-80304)

###Crash!

![smashed mount](smashed.jpg)

You've just crashed your Parallax ELEV-8 drone testing some new code. The motormounts are smashed so you check if you can...

###Buy directly from Parallax

![721-80304.png](721-80304.png)

https://www.parallax.com/product/721-80304

Parallax sells exact replacements for only $3 each. They are made from 0.093 inches thick black acetal.

Of course it is Friday night, so even 
if you paid for overnight shipping, you are grounded at least for the next 5 days. What do you do?

###Make your own replacement motor mounts!

I assume you do if you are writing drone code that you have access to a laser cutter or CNC milling machine. 

Luckily Parallax generously supplies SolidWorks model for all the parts in the ELEV-8!

###Orginal file

This is the SolidWorks file...

[721-80304.SLDPRT](721-80304.SLDPRT)

But SolidWorks is crazy expsensive, so instead I imported the part into...

###OnShape

...which is a free and pretty nice web-based 3D cad program that happens to be able to import SolidWorks files. 

Here is what I ended up with...

![OnShape](OnShape.png)

https://cad.onshape.com/documents/87f6dc6947cb4aeb3c7f5888/w/89525256ab03b4d9a79cea25/e/45e0d6c32f898424b1c1b571

From there, I exported the face to a flat R13 DXF file...

[721-80304 - Face.dxf](721-80304 - Face.dxf)

...hoping I could import than into Inkscape and then export to an SVG and send on down to the laser cutter. 

Saldy, Inkscape balked at the DXF (as often happens with DXF files) so no joy on this path.

Starting over again, I imported the SolidWorks model into...

###Fusion 360 

...which is a free and nice desktop-based 3D cad program that can also import SolidWorks files.

Here is what I ended up with...

![Fusion 360.PNG](Fusion 360.PNG)

http://a360.co/2clur11

...and again exported as a DXF...

[721-80304 - Face F360.dxf](721-80304 - Face F360.dxf)





###DipTrace file






