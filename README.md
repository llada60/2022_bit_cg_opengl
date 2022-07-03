# 2022_bit_cg_opengl

本项目是BIT 2022年图形学课程的期末大作业。

## 一、项目介绍

### 1、场景介绍

本项目为海面太阳高升的场景。天空上有飞机，海面上有小船，接近海平线有一座金碧辉煌的宝塔，并且位于远处的物体被雾所遮挡。

### 2、交互介绍

**1.鼠标移动**

鼠标移动可以直接控制视角。

**2.鼠标滚轮滑动**

鼠标滚轮滑动可以直接对场景进行放大或缩小。

**3.按键操作**

按键w(↑)、a(←)、s(↓)、d(→)分别控制视点向上、左、下、右移动。

### 3、引用的第三方库

- glad库：用于访问opengl的规范化接口的第三方库。
- GLFW库：用于图形、窗口、渲染等的第三方库。
- glm库：用于进行向量和矩阵的数学计算。
- assimp库：读取和加载obj模型
- stb_image.h：用于读取图片

### 4、代码介绍

**1.游戏控制器GameController.h：**用于鼠键交互的控制。

- updateGameController(GLFWwindow* window) ：在GLFW渲染循环中调用，用于处理逐帧的操作

**2.照相机camera.h：**用于控制调整观察视点。

   	成员变量：

- Position：相机坐标

- Front：相机前朝向向量
- Up：相机上朝向向量
- Right：相机右朝向向量
- Pitch：相机俯仰角
- Yaw：相机摇动角

**3.地面Floor.h：**绘制地面，并贴图。

**4.天空盒skyboxcube.h：**绘制天空盒作为背景。

**5.网格mesh.h：**将读入的模型绑定在网格上，实现模型的绘制和贴图。

**6.模型加载model.h：**读取obj文件，并加载模型的顶点、面、法向量、纹理等，并绘制模型。

**7.着色器shader.h：**编译、链接顶点着色器和片段着色器。

**8.纹理texture.h：**加载和绑定纹理

## 二、XML类图及主要方法注释

![img](https://uploader.shimo.im/f/u4tIY9e7FBrQY9AY.png!thumbnail?accessToken=eyJhbGciOiJIUzI1NiIsImtpZCI6ImRlZmF1bHQiLCJ0eXAiOiJKV1QifQ.eyJhdWQiOiJhY2Nlc3NfcmVzb3VyY2UiLCJleHAiOjE2NTY4NDU3MTIsImZpbGVHVUlEIjoiS3JrRVZFNWw1eUNMUFZBSiIsImlhdCI6MTY1Njg0NTQxMiwidXNlcklkIjo1Mzc3Njc4MX0.kUyu9AIL8JdcSbobTZesimycEg6DyGFA-QS3pT1v_eg)