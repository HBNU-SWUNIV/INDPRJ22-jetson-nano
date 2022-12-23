# Source Code
## Getting Started
### Environment
 - python 3.6.9
 - trt_pose 0.0.1
 - pytorch 1.0.0a0
 - sklearn 0.24.2
### Prerequisites
**Step 1 - Download PyTorch and Torchvision for Jetson nano. [link](https://forums.developer.nvidia.com/t/pytorch-for-jetson/72048)**   
**Step 2 - Install [torch2trt](https://github.com/NVIDIA-AI-IOT/torch2trt)**
```
$git clone https://github.com/NVIDIA-AI-IOT/torch2trt
$cd torch2trt
$sudo python3 setup.py install --plugins
```
**Step 3 - Install other miscellaneous packages**
```
$sudo pip3 install tqdm cython pycocotools
$sudo apt-get install python3-matplotlib
```
**Step 4 - Install trt_poses**
```
$git clone https://github.com/NVIDIA-AI-IOT/trt_pose
$cd trt_pose
$sudo python3 setup.py install
```
**Step 5 - Install dependecies for hand pose**   
```
$pip install traitlets
```
**Step 6 -  Download model weight**
| Model | Weight |
|-------|---------|
| hand_pose_resnet18_baseline_att_224x224_A | [download model](https://drive.google.com/file/d/1NCVo0FiooWccDzY7hCc5MAKaoUpts3mo/view?usp=sharing) |
- Download the model weight using the link above.   
- Place the downloaded weight in the [model](model/) directory

**Step 7 -  Open and follow robot_control_with_hand_gestures.ipynb notebook**

## Issues
If you got TLS block issue when import the sklearn in ipynb, add this
```python
import os
os.environ['LD_PRELOAD']='<your sklearn path>/scikit_learn.libs/libgomp-d22c30c5.so.1.0.0'
```

## Customize
Moving the Robot in real world you should have to change the parameters of Robot movements  for adaptable real world
```python
if gesture_joints == 1: # stop
    robot.stop()
elif gesture_joints == 2: # left
    # at here
elif gesture_joints == 3: # forward
    # at here
elif gesture_joints == 4: # right
    # at this
elif gesture_joints == 5: # backward
    # at this
else:
    robot.stop()   
```

## References
- [JetCam](http://github.com/NVIDIA-AI-IOT/jetcam) - An easy to use Python camera interface for NVIDIA Jetson
- [JetBot](http://github.com/NVIDIA-AI-IOT/jetbot) - An educational AI robot based on NVIDIA Jetson Nano
- [trt_pose](https://github.com/NVIDIA-AI-IOT/trt_pose) - Real-time pose estimation accelerated with NVIDIA TensorRT
- [trt_pose_hand](https://github.com/NVIDIA-AI-IOT/trt_pose_hand) - Real-time hand pose estimation based on trt_pose
- [deepstream_pose_estimation](https://github.com/NVIDIA-AI-IOT/deepstream_pose_estimation) - [trt_pose](https://github.com/NVIDIA-AI-IOT/trt_pose) deepstream integration
- [ros2_trt_pose](https://github.com/NVIDIA-AI-IOT/ros2_trt_pose) - ROS 2 package for "trt_pose": real-time human pose estimation on NVIDIA Jetson Platform
- [torch2trt](http://github.com/NVIDIA-AI-IOT/torch2trt) - An easy to use PyTorch to TensorRT converter