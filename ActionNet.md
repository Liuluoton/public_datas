# ACTION-Net数据集详细描述

## 1. 数据集概述
ACTION-Net模型在以下三个数据集中进行了验证：
- **Something-Something V2**：包含大量日常动作视频，涵盖丰富的时空交互。
- **Jester**：专注于手势识别，包含多种手势动作。
- **EgoGesture**：以第一人称视角采集的手势数据集，适用于人机交互场景。

## 2. 数据采集设备
| 数据集名称          | 采集设备描述                     | 分辨率       | 帧率   |
|---------------------|----------------------------------|-------------|--------|
| Something-Something V2 | 多样化设备（未明确指定）         | 多种分辨率  | 未明确  |
| Jester              | 标准摄像头                       | 未明确      | 未明确  |
| EgoGesture          | 头戴式摄像头（如GoPro）          | 高清        | 30fps  |

## 3. 数据内容与结构
- **Something-Something V2**：  
  - 内容：日常动作视频（如“拿起某物”、“放下某物”）。  
  - 结构：视频文件 + 标注文件（动作类别及时间戳）。  

- **Jester**：  
  - 内容：手势动作视频（如“滑动”、“捏合”）。  
  - 结构：视频按动作类别分文件夹存储，附带类别标签。  

- **EgoGesture**：  
  - 内容：第一人称手势视频，包含复杂背景和光照变化。  
  - 结构：视频 + 元数据（手势类别、手部位置等）。  

## 4. 关键文件说明
- **视频文件**：MP4或AVI格式，存储原始动作序列。  
- **标注文件**：JSON或CSV格式，包含动作类别、时间范围及其他元数据。  
- **预处理脚本**：用于视频帧提取、归一化或数据增强（如ACTION-Net提供的Dockerfile）。  

## 5. 数据应用场景
- **智能监控**：识别异常行为（如跌倒、闯入）。  
- **人机交互**：VR/AR中的手势控制。  
- **体育分析**：运动员动作分解与优化。  
- **医疗康复**：患者康复动作的准确性与进度评估。