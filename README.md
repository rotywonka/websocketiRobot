# websocketiRobot

Connecting to iRobot

```
   cd create_ws/
   . ./devel/setup.bash
   roslaunch ca_driver create_2.launch config:=/home/pi/create_ws/src/create_autonomy/ca_driver/config/default.yaml desc:=false

```

Setup rosbridge

```
    sudo apt-get install ros-kinetic-rosbridge-suite -y
    roslaunch rosbridge_server rosbridge_websocket.launch 

```

Start python webserver

```
    mkdir html
    git clone https://github.com/rotywonka/websocketiRobot/
    cd html
    nano test2.html
    **change url to ip address [url : 'ws://[ip address]:9090']**
    

```
