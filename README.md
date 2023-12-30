# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1: 
Take the Ep core robot insert the battery and check the battery percentage


Step2:
Turn on the robot and connect the robot to the computer through WIFI


Step3:
Open visual studio and import robomaster package and do all the code


Step4:
Take the measurment of the track on each and every turn and gives the valuse through code in (m)


Step5:
run the program to see the robot movement



## Program
```
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

    ep_chassis.move(x=0.8, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=15, xy_speed=0).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
 
    ep_chassis.move(x=0, y=2.15, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=225,g=204,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=-8, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=51,b=102,effect="on")

    ep_chassis.move(x=-1.45, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=102,effect="on")

    ep_chassis.move(x=0, y=0, z=35, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=102,g=0,b=102,effect="on")

    ep_chassis.move(x=0, y=-1.5, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=135, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=102,b=255,effect="on")

    ep_chassis.move(x=1.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=204,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=110, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=102,effect="on")

    ep_chassis.move(x=-0.97, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=128,effect="on")

    ep_chassis.move(x=0, y=-0.6, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=255,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=72, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=128,b=0,effect="on")

    ep_chassis.move(x=2.35, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
    
    
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

Insert image here

![1](https://github.com/Arun2005-create/mobilerobot-openloopcontrol/assets/138849356/8cbad991-afbf-4f10-96f9-6992c1d4442d)

![2](https://github.com/Arun2005-create/mobilerobot-openloopcontrol/assets/138849356/7f9680e3-477d-4992-a722-a121d057ff98)

![3](https://github.com/Arun2005-create/mobilerobot-openloopcontrol/assets/138849356/978ee60b-0106-4470-96ae-1fe0d3012180)


## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here


https://youtu.be/ao98DlBlQ1s?feature=shared

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
