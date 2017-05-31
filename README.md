# websocketiRobot

Connecting to iRobot [one separate window]

```
   cd create_ws/
   . ./devel/setup.bash
   roslaunch ca_driver create_2.launch config:=/home/pi/create_ws/src/create_autonomy/ca_driver/config/default.yaml desc:=false

```

Setup rosbridge  [one separate window]

```
    sudo apt-get install ros-kinetic-rosbridge-suite -y
    roslaunch rosbridge_server rosbridge_websocket.launch 

```

Start python webserver  [one separate window]  

```
    
    git clone https://github.com/rotywonka/websocketiRobot/
    mv websocketiRobot html 
    cd html
    nano test2.html
    **change url to ip address [url : 'ws://[ip address]:9090']**
    python -m SimpleHTTPServer 8080
    **open browser with your ip address and port 8080**

```

Turning on kinect  

```
       apt-cache search openni | grep ros
       sudo apt-get install ros-kinetic-openni2-launch
       apt-cache search web | grep video
       sudo apt-get install ros-kinetic-web-video-server
       roslaunch openni2_launch openni2.launch
       
```

*in another tab* Connect to web_video_server (assumes that you turned on kinect already)

```

       rosrun web_video_server web_video_server

```
       
