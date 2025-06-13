# 基于ResNet的人脸识别实现

## 简介

本部分是《人脸识别系统的设计与实现》项目的Demo2，基于facerecognition库提供的ResNet训练得到的模型实现

## 结构

- main.py 程序菜单
- get_data.py 已有人脸数据采集
- detect.py 新人脸识别
- dataset 存储拍摄的已有人脸的照片

## 原理

1. 采集人脸信息模块

   - 采集已有人脸数据集

     - 调用摄像头拍摄

     - 按格式存储图片

2. 识别人脸信息模块

   - 提取已有人脸特征

     - 基于HOG 算法给图片编码，得到处理后的图像。

     - 把上一步得到的面部图像放入训练得到的模型中，神经网络找到 128 个特征测量值并保存这 128 个测量值。

   - 识别新人脸并比较
     - 调用摄像头并重复上述步骤
     - 将摄像头拍摄人脸提取得到的128个特征值与原有特征值比对
   -  在图像上标记锚框和识别结果


## 使用

1. 环境配置
   - Python + requirements.txt
2. 运行main.py

​		





​			