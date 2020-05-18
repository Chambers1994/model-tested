# - 模型性能比较


| 场景 | 模型 | 环境 |GTX1060 | GTX1070 | GTX1080TI | GTX2080TI | i7-9550 | ARM-RK3399 | ARM-RK3399 Pro |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 目标检测 | yolov3 | keras | 100ms | 80ms | 60ms | 50ms | -| -| - | 
| 目标检测 | yolov3-tensorRT | keras | - | - | 25ms | - | 65ms| -| - | 
| 目标检测 | yolov3-tiny | keras | - | - | - | - | -| 300ms| - |
| 目标检测 | darknet | c | - | - | - | - | -| -| - | 
| 目标检测 | darknet-tiny | c | - | - | - | - | 10ms| -| - | 
| 目标检测 | mobilenetv3-ssd | python | - | - | - | - | -| -| - |
| 人脸识别 | deepface | python | - | - | - | - | -| -| - |
| 人脸检测 | libfacedetect | c | - | - | - | - | -| 20ms| - | 
| 人脸检测 | dbface | pytorch | - | - | - | 100ms | -| -| - | 
| 姿态检测 | openpose | python | - | - | - | - | -| 40ms| - | 
| 姿态检测 | openpose-tiny | python | - | - | - | - | - | 10ms | -| 
| 图像分类 | efficientNet | python | - | - | - | - | - | - | -| 
