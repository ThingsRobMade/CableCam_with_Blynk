Look, up in the… ceiling!
==========================
### How about some drone-style footage, indoors, and without a drone? It might be easier than it sounds!


Like millions of people around the world, I spent the last month watching as many World Cup matches as I could blast at my face. ([Allez les Bleus!](https://www.huffingtonpost.fr/2018/07/15/champions-du-monde-les-images-des-champs-elysees-apres-la-victoire-des-bleus-en-coupe-du-monde_a_23482490/)) But unlike most, I spent a large part of that time watching the often dizzying Cable Camera feeds. Now we all know that overhead shots and UAV-style video are big right now - try to find a decent real estate listing that doesn’t have a drone shot of the property. However, people tend to get a little squirrely when there’s a drone buzzing overhead indoors. So I wanted to see if I could make a fast and simple Cable Cam unit - the hacker’s version of what I had been watching  all month - using a few parts and a 3D printer.

![Eye in teh sky](https://user-images.githubusercontent.com/3188387/42844451-34f68bf0-89d0-11e8-93c5-2ab31bc01db9.jpg)

I have been working in 3D computer design for a really long time. How long, you ask? My early 3D design and animation work was done on an [Amiga 500 computer](https://en.wikipedia.org/wiki/Amiga_500). It was, at the time, quite a bit more advanced and a lot less expensive than anything else being offered. I’ve worked with, among other programs, [Sculpt 3D](https://en.wikipedia.org/wiki/Sculpt_3D), [trueSpace](http://www.flat2d.com/Truespace_en.aspx), TurboSilver, [Imagine](http://www.studiorola.com/tutorials/software-programs/imagine-3d-for-windows/), [Lightwave 3D](https://www.lightwave3d.com/), [Blender](https://www.blender.org/), [Vectorworks](http://www.vectorworks.net/en), and [SolidWorks](https://www.solidworks.com/). But most of these programs are either outdated, not ideally suited for this particular task, or prohibitively expensive for the average hobbyist. So I thought it was time to learn another modelling program that is more readily available, and well suited for this particular build. [Fusion 360](https://www.autodesk.com/products/fusion-360/overview) seemed like an excellent choice. And while the trial version does have a countdown clock with number of days until you need to register (at a cost of $310 a year, or $1535 for Fusion 360 Ultimate), if you are a student, teacher, educational institution, hobbyist, or small business making less than $100,000 per year, there is a free license that you can use. And you still get the full program. A sweet deal, really!

![Then and now](https://user-images.githubusercontent.com/3188387/42864416-977e7b04-8a23-11e8-96e9-c87f0c7b4b3a.jpg)
##### Billiards, 1991, designed in trueSpace: [robot safe cracker](https://www.sparkfun.com/sparkx/blog/2341)designed in SolidWorks

3D design is really just a series of adding and subtracting shapes to achieve your desired object. Want a box? Start with a rectangle, pull it up into a cube, then remove a smaller cube from the middle. Voila, a box! Want to add a screw hole? Remove a circle from it. In its simplest form, that is the essence of 3D design. More advanced designs will get into deformation, mirroring, extrusions, and a ton of other options. But everything you 3D print is ultimately just a combination of more basic shapes.

Opening up Fusion 360, the user interface is fairly intuitive. Admittedly, it helps me a great deal to be as familiar with general 3D modelling as I am. Knowing the difference between a chamfer and a fillet, or a revolve and a sweep, allow me to move quicker, create faster, and get less frustrated trying to figure out how to get the program to do what I want to do. It’s one thing to know that you don’t want two faces to meet at a hard right angle, but rather, have a soft curve between them - but modelling will be much easier and quicker if you know that a fillet. That all comes with time, and there will be frustration along the way. But you can always undo steps, and try something else, and undo that, and try something else, until you get the desired result. In fact, Fusion 360 has a timeline of each step of your build along the bottom of the window. You can go back to certain steps, move through the steps, or even play them using the play button next to the timeline.

A quick search gave me an idea of what a CableCam might look like. From there, I created some shapes, basing its size on components I planned on using, chief among them my cheap sports camera, and our [Pan/Tilt Bracket Kit](https://www.sparkfun.com/products/10335). Some of the known objects I planned to use already had existing models, like the [Right Angle Motor](https://www.sparkfun.com/products/13258), and the [Servo Motors](). [GrabCad[() is a great resource for existing models, and they are free. Fo higher end stuff, you can try sites like [Turbo Squid](https://www.turbosquid.com/), whose models range from free to “Well, if I sell my car…” The components that I created were the main body of the unit (in two halves, left and right), the drive pulley on the DC motor, and the two idler pulleys on either side of the unit. To make sure I was creating things in the right size, I also made models of the pan/tilt bracket and the [Lithium Ion Battery Pack - 2.2A](https://www.sparkfun.com/products/14169), as well as the Thing Board itself. I did all of this simply using calipers.

![The 3D environment](https://user-images.githubusercontent.com/3188387/42799090-a3dcd100-8953-11e8-94b9-4295208d96c6.jpg)
##### The 3D environment in Fusion 360

![The results](https://user-images.githubusercontent.com/3188387/42844458-3aacb812-89d0-11e8-9c17-617a0aa78a6e.jpg)
##### The printed parts. I didn't bother cleaning them up with acetone, just straight from bed to build.

As my focus for this build was more on the 3D printed elements than the electronics, it admittedly is not the most elegant solution. But the aim was speed and simplicity, which I think I achieved that. [A Sparkfun ESP8266 Thing](https://www.sparkfun.com/products/13231) and a [TB6612FNG Dual Motor Driver](https://www.sparkfun.com/products/14451) run the whole operation, along with a pair or servo motors, and a micro gearmotor. I’m using the [2.2Ah Lithium Ion Battery Pack](https://www.sparkfun.com/products/14169) for its 5V output. And the Blynk app made control a breeze.

### IF AT FIRST YOU DON’T SUCCEED

My first attempt used a [Right Angle Hobby Motor](https://www.sparkfun.com/products/13258) because I knew it would be simple to mount, and TBH, I had one on my desk within arm’s reach. This proved to lack the torque needed to move the CableCam consistently, but also gave me a little insight on the drive pulley. While there were times when the motor would simply stall, there were also times when the drive pulley would just slip, so I wound up adding a bit of texture inside the drive pulley for its final build. And by texture, I mean cool spikes!

![](https://user-images.githubusercontent.com/3188387/42847419-1ff366ca-89d9-11e8-937f-0f3510b8d4b9.jpg)
##### So punk!

At first I thought I would have to alter and reprint the entire frame. However, looking at the housing for the new, smaller motor, it’s placement dictated that it would be simpler to just create a small extension that attached to the back of the existing frame, onto which the motor housing could easily be mounted. I also placed the battery holder on the front to better balance the unit, and added holes so that it would also be possible to use the [Pi Cam in the smaller pan/tilt bracket](https://www.sparkfun.com/products/14329). This could allow for streaming video, but that’s a post for another day.

![Blynk Screen Grabs](https://user-images.githubusercontent.com/3188387/42799096-a8a83ce2-8953-11e8-91c0-7bf88df9e251.jpg)

##### The Blynk app, with settings for both the Rig Motor and the Pan/Tilt control

The [Blynk app](https://www.blynk.cc/) is incredibly intuitive to use. Add a component, set what that component does, connect to your project, and Bob’s your Uncle. You’ll notice that I have the rig speed range set from 0 to 100. In the code uploaded to the Thing, we map this to a range of -255 to 255. The reason for this were twofold; the Blynk app won’t accept a negative number for this output range, but the motor driver uses positive integers to travel one direction, and negative integers to travel the other. And the reason I didn’t use a range of 0 to 510 is because I wanted the center range, where the motor sits idle, to be a bit easier to hit. I also make sure that the rig speed control slider is always at center on startup, so the CableCam doesn’t immediately take off.

VIDEO or GIF HERE

So as you can see in the video, the servo motion is a little jerky, and it causes a bit of swing on the cable when it moves. IN addition, the travel speed was much slower than I had hoped. BUt over an eighty foot span, quite a lot of pressure was placed on the motor. It would take some experimenting to find the sweet spot between torque and speed. But since this build was more about 3D printing the rig than creating something that FIFA or the NFL or even the local theatre is going to be clamoring for, I think it was a success.  The toughest part about 3D printing is the design phase. Lots of people get a 3D printer, and then just download existing files to print. And that certainly has its place. But the first time that you visualize something that doesn’t currently exist, and are able to design it on the computer, and a few hours later be holding it in your hand... Well that, friends, is a feeling that stays with you. Now go out there and start seeing everything around you as the collection of primitive shapes that it is!

![My first 3D print](https://user-images.githubusercontent.com/3188387/42844432-221ff2b4-89d0-11e8-8546-33fca0120bf5.jpg)
##### Where it all began. My first idea-to-object 3D print.

You can find a wishlist of all the parts [here](https://www.sparkfun.com/wish_lists/147123).

Code and .stl files are in [this Github repository](https://github.com/RTR52nd/CableCam_with_Blynk).