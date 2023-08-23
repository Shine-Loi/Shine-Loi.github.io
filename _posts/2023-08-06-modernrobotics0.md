---
title:  "[Modern Robotics] Chapter 0. Overview"
excerpt: "Overview of Modern Robotics"

categories:
  - Modern Robotics
tags:
  - [Robotics, Modern Robotics, Overview]

toc: true
toc_sticky: true
 
date: 2023-08-06
last_modified_at: 2023-08-23
---

&nbsp;

# 1. 개요
로봇공학은 궁극적으로 사람처럼 행동하고 생각할 수 있는 기계를 만드는 것을 목표로 한다.\
이 카테고리에서는 Kevin M Lynch, Frank C Park 저자의 **Modern Robotics: Mechanics, Planning, and Control** 교재를 중심으로 공부하는 내용을 정리할 예정이다.

&nbsp;

&nbsp;

&nbsp;

# 2. 챕터 요약
이 카테고리에서 다루는 내용은 다음과 같다.

&nbsp;

## 2-1. Configuration Space(상태 공간)
로봇의 모든 점의 위치를 명시하는 로봇 시스템의 Configuration을 설명하는 챕터이다.\
로봇 메커니즘의 자유도, Configuration Space의 위상과 표현법 등을 배운다.

&nbsp;

[Chapter 1-1. Degrees of Freedom of a Rigid Body](https://shine-loi.github.io/modern%20robotics/modernrobotics1-1/)\
[Chapter 1-2. Degrees of Freedom of a Robot](https://shine-loi.github.io/modern%20robotics/modernrobotics1-2/)\
[Chapter 1-3. Configuration Space: Topology and Representation]()\
[Chapter 1-4. Configuration and Velcity Constraints]()\
[Chapter 1-5. Configuration and Velocity Constraints]()\
[Chapter 1-6. Summary]()\
[Chapter 1-7. Exercises]()

&nbsp;

## 2-2. Rigid-body Motions(강체 운동)
3차원 물리적 공간에서 강체의 움직임을 수학적으로 묘사하는 방법에 대해 설명하는 챕터이다.\
행렬과 Exponential Coordinate 표현 등을 배운다.

&nbsp;

[Chapter 2-1. Rigid-Body Motions in the Plane]()\
[Chapter 2-2. Rotations and Angular Velocities]()\
[Chapter 2-3. Rigid-Body Motions and Twists]()\
[Chapter 2-4. Wrenches]()\
[Chapter 2-5. Summary]()\
[Chapter 2-6. Software]()\
[Chapter 2-7. Exercises]()

&nbsp;

## 2-3. Forward Kinematics(정기구학)
관절의 값이 주어질 때 엔드 이펙터에 붙은 기준 좌표계의 위치와 방향을 계산하는 방법을 배운다.

&nbsp;

## 2-4. Velocity Kinematics and Statics(속도 기구학과 정역학)
관절 속도와 엔드 이펙터 좌표계의 선속도와 각속도 사이의 관계를 나타내는 속도 기구학을 해석하기 위한 자코비안에 대해 배운다.

&nbsp;

## 2-5. Inverse Kinematics(역기구학)
엔드 이펙터 Configuration을 얻기 위한 관절 변위를 계산하는 방법을 배운다.

&nbsp;

## 2-6. Kinematics of Closed Chains(폐연쇄의 기구학)
개연쇄는 유일한 정기구학 해를 가지지만 폐연쇄는 다수의 정기구학 해 또는 다수의 역기구학 해를 가지기도 한다.\
또한 폐연쇄는 구동되는 관절과 수동적인 관절 모두 가지기 때문에 개연쇄에서는 나타나지 않는 이슈들이 존재한다.\
이 챕터에서는 폐연쇄의 기구학 분석을 위한 기본 개념에 대해 배운다.

&nbsp;

## 2-7. Dynamics of Open Chains(개연쇄의 동역학)
정동역학 문제는 주어진 관절 힘과 토크에 대해 관절 가속도를 계산한다.\
역동역학 문제는 주어진 관절 가속도를 생성하기 위해 필요한 입력 관절 토크와 힘을 계산한다.\
이 챕터에서는 로봇의 동역학 방정식의 해석적 유도와 정동역학, 역동역학에 대한 재귀적 알고리즘을 배운다.

&nbsp;

## 2-8. Trajectory Generation(궤적 생성)
로봇이 자동화 기계와 차별화되기 위해서는 다양한 업무를 위해 쉽게 재프로그래밍이 가능해야 한다.\
서로 다른 작업을 위해 필요로 하는 동작들은 서로 다르고, 사용자가 모든 작업에 대한 궤적을 직접 명시하는 것은 거의 불가능하다.\
즉 로봇은 특정한 작업을 나타내는 몇 가지 입력 데이터를 통해 스스로 동작을 생성해야 한다.

&nbsp;

## 2-9. Motion Planning(동작 계획)
이 챕터에서는 비정형의 작업 공간 사이로 관절 한계, 구동기 한계, 로봇에 부과된 다른 물리적 제약을 피하며 로봇의 충돌 회피 동작을 찾는 문제를 배운다.

&nbsp;

## 2-10. Robot Control(로봇 제어)
로봇 제어기의 역할을 어떤 작업에 대한 서술을 구동기 힘과 토크로 변환하는 것이다.\
이를 위해 위치 제어, 힘 제어, 하이브리드 운동-힘 제어, 임피던스 제어 등에 대해 배운다.

&nbsp;

## 2-11. Grasping and Manipulation(파지와 조작)
이 챕터에서는 로봇과 물체 사이의 접촉에 대한 모델링 방법을 배운다.

&nbsp;

## 2-12. Wheeled Mobile Robots(차륜 이동 로봇)
이 챕터에서는 로봇 팔을 갖춘 차륜 이동 로봇의 기구학, 동작 계획, 제어를 다룬다.

&nbsp;

&nbsp;

&nbsp;

# 3. 참고
이 카테고리는 다음 내용을 참고하여 작성할 예정이며 추가로 참고하는 자료는 각 포스트에 별도로 표기할 계획이다.
1. Kevin M Lynch, Frank C Park.Modern Robotics: Mechanics, Planning, and Control
2. [Coursera, Northwestern University, Modern Robotics 강좌](https://www.coursera.org/?skipBrowseRedirect=true)