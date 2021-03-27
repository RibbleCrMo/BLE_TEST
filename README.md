 How to use 1000M time trial site

 When 1000M time trial using a roller, measure time measurement and movie shooting and saving. Use the speed sensor compatible with Bluetooth Low Energy (BLE). Speed ​​Cadence An integrated sensor is also OK. Mainly made use of Windows 10 Microsft Edge.
 I think that I do not work with Internet Explorer, but it seems that Chrome or Firefox is new. I moved some of my smartphone (Android 7.0 old). Click here for video shooting using XOSS sensors. 
https://youtu.be/gw5inyje84i

 1. Enter profile
 First, enter your profile. "Name"  and "Tyre Circumstance"  are required input items. The item later is optional, but when the input is completed, press the CONFIRM button.

 2. Speed ​​sensor connection
 Press the Connect Speed ​​Sensor button. A small window opens. If you look for a pair of pairs that can be paired, it will be displayed on the window (it may take some time to find. Since the speed sensor is sleeping, it may not be found. So before connection, move the sensor slightly and raise it from the sleep state.).
 Then select the device you want to pair and press the pairing button (two sensors are detected if you are using both speed sensors and cadence sensors. In that case, choose the speed sensor. When "> Notification Started" is displayed on the "BLE STATUS" window below, the sensor is connected to indicate that the data can be obtained. If you get an error, please try pressing the Connect Speed ​​Sensor button again.

 3. start
 When the connection with the sensor is confirmed, press the START YOUR TRIAL button.
 First of all, I think that the camera is asked to use, but when you allow the camera start and display on the screen, and recording starts.
 Please be assured that you do not have to send the camera image to some server. There is image data only within the user equipment.
 After 30 seconds pressing the button, the trial will begin. The countdown is over and when a red lamp is attached.
 Actually, the number that flows like a stopwatch that appears in the TIME column is also not used for actual measurements with the number of random speech seconds and decorations. So, the speedometer rising is slow and the speed may be displayed at first at 0 km / h, but don't worry (I think that it will be displayed as 0 km / h after 1 second to 2 seconds after running. You).
 Since the mechanism of the speed sensor sends the cumulative wheel rotational speed and the time when it records it per second (unit is 1/1024 seconds), the time that recorded the first one rotation after the start (T0 It will be a second.) And the cumulative rotational speed (as C0) at that time. After the distance exceeds 1000 m, the wheel is turned to one rotation (T1 second. The number of revolutions at this time is 2096 mm (C0 + 478) rotation (C0 + 478) rotation (2096 mm x 478 rotation) From the time of the start point and the time of starting point, the time of 1000 M runs ((T1-T0) × 1000 / 1001.888).
 The measurement accuracy is a critical for the tire. If the tire is 2 mf , Since the distance was changed by 1 M, the tire peripheral length changes with the same 700 × 23C, the type of tire, wearing teeth, weight, air pressure, etc., so the time is calculated to 1/100 seconds. But be careful when comparing with other bicycle records.
 When 1000m is running, there is a goal voice and time reading and the measurement is complete. In addition, in order to avoid an infinite loop, we programped to go over within 180 seconds (6 minutes) after the start (10 km of average hour). It does not confirm what will happen if it takes more than 6 minutes to goal.

 4. About recording
 When the goal is finished automatically, a message appears with a link "Download Video File". You can download a file named "Movie.webm". When this file is played back, the information at the top of this website should be reflected. Unfortunately no voice is included.
