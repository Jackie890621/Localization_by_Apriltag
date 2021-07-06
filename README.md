# Localization_by_Apriltag
HCC final project
## Objective
### Find position of the target objects
* Pyrobot bag
  * orange bottle
  * green bottle
  * the tvmonitor/laptop closest to Tag1
  * backpack
  * teddy bear
* Drone bag
  * umbrella
  * bike
  * teddy bear
  * the chair closest to teadybear
#### rosbag download link
https://drive.google.com/drive/folders/1RA0Xk5SDDXfxqrmRWHVzmDvLAmzPE7aW
## Implementation
### Step1
You need to finish the code below:
* hcc_ws/src/estimation_pos/src/apriltag_localization.cpp
* hcc_ws/src/estimation_pos/src/drone_object.py
* hcc_ws/src/estimation_pos/src/pyrobot_object.py

Note that when you write something in the **.cpp** code, make sure to **catkin_make**
```
hcc_ws $ catkin_make
```
### Step2
After finishing your code, you are ready to test the result. Please remember whenever opening a new terminal, you have to **source the enviroment workspace**.
```
hcc_ws $ source devel/setup.bash
```
### Step3
Run ROS master on terminal(T1):
```
hcc_ws $ roscore
```
Run multiple roslaunch on terminal(T2):
```
hcc_ws $ source Run_All_"drone / pyrobot".sh
```
Generate final position by local outlier factor:
```
hcc_ws $ python output_generate.py
```
### Step4
You can test your results with the groundtruth which I put it below:

https://drive.google.com/drive/folders/15XcuJK-Hy1i9Lcs3ROwv7FiOEAIghjZG

Evaluate the outcome:
```
python eval.py "ans.txt" "ours"
```


