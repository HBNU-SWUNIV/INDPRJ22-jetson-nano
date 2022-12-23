# 한밭대학교 SW중심대학 산학연계프로젝트 - 지능형 IoT 기술 분석 및 소프트웨어 개발

## **팀 구성**
### 지도교수
 - 김은경 교수님

### 기업체 
 - 로보볼트, 정의림 대표

### 참여학생
 - 20161616 연제원
 - 20197132 주준하
 - 20181796 김민준
 - 20181602 최창수


## Project Background
- ### 필요성
  - 기존의 건설기계 장비로는 산업재해로 인한 사망자가 많음   
  - 내부 근로자의 시야가 확보되지 않고 주변을 살피지 못해 발생함.   
- ### 기존 해결책의 문제점
  - 건설장비에서 외부를 감지하는 IoT 기술만을 활용하여 안전 문제를 해결해왔음.
  - IoT장비로는 탐지할수 없는 anomaly한 상황에 취약점이 드러남.



## System Design
  - ### System Requirements
This project aims to control excavation equipment and forklifts through hand gestures. The project adapt modern deep learning using hand gesture recognition and implemented tilt pose.
This project has tested on Jetsno NANO with the following environments:
   - python 3.6.9
   - trt_pose 0.0.1
   - Pytorch 1.0.0a0
   - sklearn 0.24.2
   - Jetson Nano Robot library.

    
## Case Study
- There are many deaths caused by industrial accidents in construction machinery.   
- It is caused by the lack of visibility of internal workers and the inability to look around.   
- It can be safely operated by checking the field of view through the hand motion detection robot control system from the outside and operating heavy equipment.
<img src="https://user-images.githubusercontent.com/77065758/206336403-a47f8949-ccc9-41cb-a192-da5e64474d3e.png"  width="200" height="160"/>

### Application of ideas
- a forklift truck
 - Basic behavior of forklifts
<img src="https://user-images.githubusercontent.com/77065758/206336412-f40b8390-aea4-4b23-88b1-cd1d6e1cc2b1.jpg"  width="200" height="160"/>
  <details>
  <summary>Movement</summary>
  <div markdown="1">
    1. Forward – Backward<br>
    2. Up – Down<br>
    3. In front of tilt – back<br>
  </div>
  </details>
		After matching the basic movements of the forklift with the hand movements, the forklift is controlled with the hand movements

- an excavator
 - How the Excavator Works
<img src="https://user-images.githubusercontent.com/77065758/206336595-c14de783-47d7-410f-9a50-d5371c5761db.png"  width="200" height="160"/>
  <details>
  <summary>Movement</summary>
  <div markdown="1">
   1. Boom Cylinder (Up – Down)<br>
		 2. Handle cylinder (upper – lower)<br>
		 3. Bucket cylinder (upper – lower)<br>
  </div>
  </details>
		The excavator operates each cylinder. It is complicated to control this with hand gestures. You have to come up with an idea to pump it automatically.

- a companion robot
 - High-five, stop, and take pictures. You can express various directions
<img src="https://user-images.githubusercontent.com/77065758/206336401-a56fdcad-7dc5-427c-9a91-fcf9950dbb07.jpg"  width="200" height="160"/>
 
#### In addition to heavy equipment, I think it can be applied in various ways.  


### Related technology
- "Samsung Electronics' All-in-One PC" that recognizes hand movements and works
<img src="https://user-images.githubusercontent.com/77065758/206336409-5f9e5879-4045-40f1-b15a-8c98d7de46c2.jpg"  width="200" height="160"/>

- Amazon AI Secretary Recognizing Sign Language "Alexa"
<img src="https://user-images.githubusercontent.com/77065758/206336405-0f2eb732-3d89-445a-b0ec-84d9551e9187.png"  width="200" height="160"/>

### Introduction to ideas
- Recognizing a person's hand movements through a camera
- Robot control for each movement, and various movements can be customized.


  
## Conclusion
It can be safely operated by checking the field of view through the hand motion detection robot control system from the outside and operating heavy equipment.
The machine recognizes the following hand movements and performs the following functions.  
<details>
 <summary>Movement</summary>
 <div markdown="1">
  1. Fist = Stop<br>
  2. One finger (finger) = left<br>
  3. Palm = Go straight<br>
  4. Two Fingers (V) = Right<br>
  5. Okay = Back up<br>
 </div>
 </details>  
 
![](imgs/run.gif)
![](imgs/backward.jpg)


## Project Outcome
- ### JETSON AI SPECIALIST CERTIFICATION