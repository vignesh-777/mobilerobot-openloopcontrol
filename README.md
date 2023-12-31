# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure
### Step1: 
Take the Ep core robot insert the battery and check the battery percentage

### Step2:
 Turn on the robot and connect the robot to the computer through WIFI

### Step3:
 Open visual studio and import robomaster package and do all the code

### Step4:
 Take the measurment of the track on each and every turn and gives the valuse through code in (m)

### Step5:
 run the program to see the robot movement
## Program
```python
from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.6, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    
    ep_chassis.move(x=0.3, y=0, z=80, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    
    ep_chassis.move(x=1, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")
    
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=-1.6, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=50, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")
   
    ep_chassis.move(x=0, y=-1.35, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=-130, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=204,effect="on")

    ep_chassis.move(x=0, y=1.55, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=0,effect="on")

    ep_chassis.move(x=2.05, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=51,b=0,effect="on")
    
    ep_chassis.move(x=0, y=0, z=80, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=0.65, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=102,g=102,b=153,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=51,effect="on")



    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)
![](./Screenshot%202023-12-29%20221543.png)
## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.
https://youtu.be/SISTRUmBrcs?si=zO6BUlQT-C2KAsFY

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
