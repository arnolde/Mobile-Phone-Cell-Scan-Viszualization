
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
12591,**8175**,6,6,MON,4  
**8175**,15677,6,7,MON,11  
15677,15646,7,7,Mon,15  

Our goal is to understand and to visualize when, where and in which amount our swarm is moving. Will it be something like this? A Move from Sector-Scan to Sector-Scan. Detecting where people live, stay ( how long?), leave, work, celebrate,....

![image](https://user-images.githubusercontent.com/37293282/75032428-e0bdde80-54a8-11ea-817b-84d486c16531.png)

considering all this we generated some random ( fake ) data of such kind of "Trails":

trailNr,src_dst,src,lon,lat,date,day,hour,minute,count,v,s,t
1,8174_**8185**,8174,11.410571516906163,48.15152679449321,2017-05-01 06:00,MON,6,0,22,0,1999.0,60  
1,8174_8185,8174,11.415943928198173,48.15145741662311,2017-05-01 06:05,MON,6,5,22,0,1999.0,60  
1,8174_8185,8174,11.421316339490183,48.151388038753005,2017-05-01 06:10,MON,6,10,22,0,1999.0,60  
1,8174_8185,8174,11.42668875078219,48.15131866088291,2017-05-01 06:15,MON,6,15,22,0,1999.0,60  
1,8174_8185,8174,11.4320611620742,48.1512492830128,2017-05-01 06:20,MON,6,20,22,0,1999.0,60  
1,8174_8185,8174,11.43743357336621,48.151179905142705,2017-05-01 06:25,MON,6,25,22,0,1999.0,60
1,8174_8185,8185,11.43743357336621,48.151179905142705,2017-05-01 06:29,MON,6,29,22,0,1999.0,60
1,**8185**_15638,8185,11.43743357336621,48.151179905142705,2017-05-01 06:30,MON,6,30,20,0,1581.0,60
1,8185_15638,8185,11.441436997212305,48.15022748181894,2017-05-01 06:35,MON,6,35,20,0,1581.0,60
1,8185_15638,8185,11.4454404210584,48.149275058495164,2017-05-01 06:40,MON,6,40,20,0,1581.0,60
1,8185_15638,8185,11.449443844904495,48.1483226351714,2017-05-01 06:45,MON,6,45,20,0,1581.0,60
1,8185_15638,8185,11.45344726875059,48.14737021184762,2017-05-01 06:50,MON,6,50,20,0,1581.0,60
1,8185_15638,8185,11.457450692596685,48.146417788523856,2017-05-01 06:55,MON,6,55,20,0,1581.0,60
1,8185_15638,15638,11.457450692596685,48.146417788523856,2017-05-01 06:59,MON,6,59,20,0,1581.0,60
2,8174_8185,8174,11.410571516906163,48.15152679449321,2017-05-01 07:00,MON,7,0,40,0,1999.0,60

Assuming that our ESP-Scanner-Devices are distributed over the town - we will have up to 60m between our scanner devices ( or more ). To visualize this in Folium we extra generate some random-Points between those
Scanners. In Reality: as much of those Scanners would be distributed - as better and precize  the Scan-Results will be. One scenario would be to add this devices into Street-Lamps:


