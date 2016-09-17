# DYI-Replacement-Motormount-for-ELEV-8
Files for making your own [replacement motor mounts for the Parallax ELEV-8 drone](https://www.parallax.com/product/721-80304)

###Crash!

![smashed mount](smashed.jpg)

You've just crashed your Parallax ELEV-8 drone testing some new code. The motormounts are smashed so you check if you can...

###Buy replacements directly from Parallax

![721-80304.png](721-80304.png)

https://www.parallax.com/product/721-80304

Parallax sells exact replacements for only $3 each. They are made from 0.093 inches thick black acetal.

Of course it is Friday night, so even 
if you paid for overnight shipping, you are grounded at least for the next 5 days. So you decide to...

###Make your own replacement motor mounts!

Luckily Parallax generously supplies files for all the parts in the ELEV-8!

I have a laser cutter, and converting files into flat plastic shapes is exactly what laser cutters do! Whoo hoo, I'll have my motormount in no time!

###Orginal file

This is the SolidWorks model...

[721-80304.SLDPRT](721-80304.SLDPRT)

But SolidWorks is crazy expsensive, so instead I imported the part into...

###OnShape

...which is a free and pretty nice web-based 3D cad program that happens to be able to import SolidWorks files. 

Here is what I ended up with...

![OnShape](OnShape.png)

https://cad.onshape.com/documents/87f6dc6947cb4aeb3c7f5888/w/89525256ab03b4d9a79cea25/e/45e0d6c32f898424b1c1b571

That looks familiar! I'll take 4 to go please!

I exported the face to a flat R13 DXF file...

[721-80304 - Face.dxf](721-80304 - Face.dxf)

Now my laser cutter does not do DXF files, but I can import the DXF into...

###Inkscape

...which is a free program that can import DXF and export the SVG files my laster cutter craves!

Saldy, Inkscape balked at the DXF (as often happens with DXF files) with a "POLYLINE encountered and ignored" error so no joy on this path.

This must be my punishment for trying to use a cutting-edge web-based CAD tool. Serious people who want to get things doneuse
use monster CAD workstations running serious tools like...

 ###Fusion 360 

...which is a free and nice desktop-based 3D cad program that can also import SolidWorks files.

Here is what I ended up with...

![Fusion 360.PNG](Fusion 360.PNG)

http://a360.co/2clur11

...and again exported as a DXF...

[721-80304 - Face F360.dxf](721-80304 - Face F360.dxf)

...which again seems to make Inkscape vomit bits in the same way.

Hmmm... getting an SVG to send to the laser cutter is turning out to be a lot of work!

Luckily anyone who is building custom drone hardware also likely has an...

###Othermill PCB cutter

PCBs are sort of the right thickness and are probably strong enough, so if I can just make a PCB board that happens to 
be exactly the same shape as a motormount... Hmmm... A hack to be sure, but it should work!

Sadly the newest version of the Othermill software can not directly import a DXF file (maybe someday Othermill poeple? Please?).

Luckily, I definately can import DXF files into...

###DipTrace PCB layout software

...which happy imported the DXF with ease! I specified to import the "visible" layer from the DXF into the "Board Outline" layer of the 
board and ended up with a motormount shaped board!....

![DipTrace Outline.PNG](DipTrace Outline.PNG)

I am so close I can taste it! I quickly exported the board outline to a gerber file...

![gerber.png](gerber.png)

[BoardOutline.gbr](BoardOutline.gbr)

...and jogged over to mill to load the file into...

###Otherplan

...which is the software that reads in gerber files and actually cuts the boards on the Othermill.

Hey! I have a gerber and I want a board, so I the rest is just ceremony- right?

Wrong!!! Turns out that Otherplan can not even load my gerber file! It has not implemented the gerber "G85" command 
which is used to describe internal cutouts. Boo Hoo (maybe someday OtherMill people? Please?).

Luckily those internal cutouts happen to be exactly round circles so if can conver the cutouts to...

###Drill hits

I can create a gerber file for the outside outline of the shape, and then create an Excelon drill hits file for the 
interior cut-outs!

This turns out to be slightly tedious becuase I have to manually measure the cutouts and then carfully center the drill
hits in the middle of each cutout, but eventually I end up with this... 

![DipTrace Outline With Drill Hits.PNG](DipTrace Outline With Drill Hits.PNG)

...from which I can generate an outline gerber...

![Outline Gerber No Holes.PNG](Outline Gerber No Holes.PNG)

[BoardOutline No Holes.gbr](BoardOutline No Holes.gbr)

...and a drill hits file...

![Drill Hits.PNG](Drill Hits.PNG)

[Through.drl](Through.drl)













###DipTrace file






