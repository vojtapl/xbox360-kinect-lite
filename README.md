# Pcb and Case for Shrinking the Xbox 360 Kinect
This repository contains a PCB and a basic case for using only the camera board from the Xbox 360 Kinect.

I have recently read [this great article](https://medium.com/robotics-weekends/how-to-turn-old-kinect-into-a-compact-usb-powered-rgbd-sensor-f23d58e10eb0), which lays out the idea of making a *Kinect Lite* from an old Xbox 360 Kinect by isolating the camera board, which can function separately. As I saw one being sold for next to nothing with a broken tilt motor, I thought it would be a great idea to implement the ideas mentioned in the article. The repository contains the PCB (including LCSC part numbers), which generates all the necessary voltage rails, and a basic 3D-printable case.

## What might need improving
- The case model is a bit crude, as I used this as a opportunity to learn some basics of FreeCAD. Also, the camera PCB screws do not seem to be arranged in a rectangle, so one of the mounting holes might need enlarging.
- The case walls are a bit too long and flex a bit when squeezed.
- I am uncertain whether the fan and the fuse (not really sure what exactly it is) on the IR transmitter is really needed.

## Assembly
0. Acquire the Xbox 360 Kinect, make the PCB, and print the case.
1. Tear down the Kinect. [Example video.](https://youtu.be/PgViFpEWwBA)
2. What we will need from it is the PCB to which the cameras are connected (without the LED, as it connects to a PCB which we will not use), the aluminum chassis with the cameras, the cooling fan, some of the screws and standoffs, and the lens plastic holder with the lenses.
3. Cover the cameras and the IR transmitter with tape and cut the aluminum chassis with a saw next to the cameras. One cut will be next to the two cameras - when looking from the inside - right next to the white plastics, and the other will just remove the bent part next to the IR transmitter. See the photos of how it should look afterward. Remember to clean everything from the shavings.

![cut chassis](https://github.com/vojtapl/xbox360-kinect-lite/blob/main/images/cut%20chassis.png?raw=true)

4. Get the case and add the lenses (note that the IR projector one has a small notch) and insert them into the case. Add the plastic holder on top and screw it in (it might need a corner cut).
5. Insert the PCB correctly onto the camera PCB - either use the standoffs with the included screws and then push the small connector in, or push the connector in first so that the small connector connects to the middle pins (with one row on the left and one on the right unconnected). Now is a good time to test things out.
6. Screw the camera PCB into the cut aluminum chassis and connect the cameras, fan, and the IR transmitter (every cable should be connected by now).
7. Insert the fan with the cable sticking up and the rubber padding away from the air intake.

![case with fan](https://github.com/vojtapl/xbox360-kinect-lite/blob/main/images/case%20with%20fan.png?raw=true)

8. Screw in the chassis assembly.
9. Screw in the back plate, and you are done.

## Power consumption
The measurements were made with KWS-2301C, a cheap USB-C power meter.
- Idle
![Idle power consumption](https://github.com/vojtapl/xbox360-kinect-lite/blob/main/images/power%20consumption%20idle.png?raw=true)
- Running with `freenect-regview`
![Idle power consumption](https://github.com/vojtapl/xbox360-kinect-lite/blob/main/images/power%20consumption%20running.png?raw=true)

## Images
On the ruler look at the top scale, as that one is in centimeters.
- View from right
![View from right](https://github.com/vojtapl/xbox360-kinect-lite/blob/main/images/view%20from%20right.png?raw=true)
- View from side
![View from side](https://github.com/vojtapl/xbox360-kinect-lite/blob/main/images/view%20from%20side.png?raw=true)
- View from above
![View from above](https://github.com/vojtapl/xbox360-kinect-lite/blob/main/images/view%20from%20above.png?raw=true)
- PCB
![PCB](https://github.com/vojtapl/xbox360-kinect-lite/blob/main/images/pcb.png?raw=true)

