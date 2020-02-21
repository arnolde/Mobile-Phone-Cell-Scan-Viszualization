
**Mobile-Phone Swarm-Motion Detection, Mass-Data-Analysis and Visualization**



WTF?

Imagine you have some kind of Motion-Data. The motion from Mobile-Phone-Devices over an geographic Aera.

![image](https://user-images.githubusercontent.com/37293282/75029501-70ac5a00-54a2-11ea-950a-72819bf253d1.png) ![image](https://user-images.githubusercontent.com/37293282/75025059-cb41b800-549a-11ea-8e0f-a6b44bbb966a.png)

We would need hundrets or thousends of such kind of ESP8266-Mobile-Device-Scanners to cover a big Town ( like Munich ) . 

Finally we took the Data from some of our scans..and generated the rest of this kind of data. This way the data we observe here **is a simulation** ...some kind of **fake-Data**. So we take this data as given!

But bear in Mind - the technology behind all this is REAL! The basic Concept on how to Measure such kind of Device-Location is described here: https://github.com/iCounterBOX/Trilateration-with-NodeMCU-8266


**The Experiment**

Our assumption is to have hundrets of those Scan-Boxes over an area..e.g Munich:

![image](https://user-images.githubusercontent.com/37293282/75027380-c67f0300-549e-11ea-837e-195551333a5f.png)

and finally we want vizualize how a target-Group ( e.g. devices at 6:00 AM ) are MOVING across this area!
An animated simulation...

![image](https://user-images.githubusercontent.com/37293282/75029173-e06e1500-54a1-11ea-99de-10ed91e3386f.png)

**Play-Data**

each Scanner-Device  ![image](https://user-images.githubusercontent.com/37293282/75030965-87a07b80-54a5-11ea-9394-e58e560dc468.png) is getting a random-ID over an Geo-Location Area. In this experiment distributed over Munich. As each Mobile device has a unique MAC - a Grid of such ESP-Scanners is easily able to store this in form of "Trails". e.g 100 Devices detected in sector A ( 6:00 AM ) ... 1 Hr later those 100 Devices also detected in Sector B - this way we have a MOVE vom Sector A to Sector B...then form Sector B to Sector C...etc etc

src,dst,time_src,time_dst,day,amount
12591,8175,6,6,MON,4
8175,15677,6,7,MON,11
15677,15646,7,7,Mon,15


