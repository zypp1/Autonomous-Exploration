# Autonomous Exploration

## Build 
```bash
git clone https://github.com/zypp1/Autonomous-Exploration.git
```
### build Livox-SDK2

```bash
cd Autonomous-Exploration/Livox-SDK2
mkdir build 
cd build
cmake ..
make
sudo make install 
```

### build src

```bash
cd Automous-Exploration
catkin_make
```

## run

### livox_ros_driver2
```bash
cd Automous-Exploration
source devel/setup.bash
roslaunch livox_ros_driver2 msg_MID360.launch
```

### fast-lio
```bash
cd Automous-Exploration
source devel/setup.bash
roslaunch fast_lio mapping_mid360.launch
```

### vehicle-simulator
```bash
cd Automous-Exploration
source devel/setup.bash
roslaunch vehicle_simulator system_real_robot.launch
```

### tare-planner
```bash
cd Automous-Exploration
source devel/setup.bash
roslaunch tare_planner explore_tunnel.launch
```

## tips

### fast-lio building

1. if using MID360, its necessary to change lidar ip '192.168.1.1XX'.'XX' is the last two numbers of the SN of the MID360.

2. if fast-lio doesn't work, please fixed the wired ip,Address: 192.168.1.5,Netmask: 255.255.255.0,Gateway: 192.168.1.1,DNS:192.168.1.1.

3. more building details: https://blog.csdn.net/Hahalim/article/details/129414327?ops_request_misc=&request_id=&biz_id=102&utm_term=%E5%A4%9Amid360%E6%BF%80%E5%85%89%E9%9B%B7%E8%BE%BE%E6%A0%87%E5%AE%9A&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-6-129414327.142%5Ev100%5Epc_search_result_base2&spm=1018.2226.3001.4187

### out put control 

1. the tare planner's output topic is /cmd_vel.

