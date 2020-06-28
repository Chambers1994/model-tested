# - 模型性能比较


| 场景     | 模型       | 环境    |GTX1060 | GTX1070 | GTX1080TI | GTX2080TI | i7-9550 |i5-9400F| SOM-RK3399 | TB-RK3399Pro |GTX1650
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |:-: |:-: |
| 目标检测 | yolov3-416 | keras   | 100ms | 80ms     | 60ms     | 50ms        | -       | -     | -           | 90ms        | - |
| 目标检测 | yolov3-416 | darknet | -     | -         |   -     | -           | -       | -     | -           |  -          | 150ms |
| 目标检测 | yolov3-416 | tensorRT| -     | -         | 25ms    | -           | 65ms     | -    | -           | -           |   - |
| 目标检测 | yolov3-tiny-416 | keras | -  | -         | -       | -           | -        | 300ms|-            | -           | - |
| 目标检测 | yolov3-tiny-416 | rknn | /   | /         | /       | /           | /         | /   |/            | 30ms        | / |
| 目标检测 | yolov3-tiny-416 | darknet | - | - | - | - | -| -|- | - | 100ms |
| 目标检测 | yolov4-608  | darknet | - | - | - | - | -| -|- | - | 270ms |
| 目标检测 | yolov5s-640  | pytorch | 20ms | - | - | - | - | 500ms |- | - | - |
| 目标检测 | mobilenetv3-ssd | python | - | - | - | - | - | - | - | - | - |
| 人脸识别 | deepface | python | - | - | - | - | - | - | - | - | - |
| 人脸检测 | libfacedetect | c | - | - | - | - | -| 20ms| - |  - | - |
| 人脸检测 | dbface | pytorch | - | - | - | 100ms | -| - | - |  - | - |
| 姿态检测 | openpose | python | - | - | - | - | -| 40ms| - |  - | - |
| 姿态检测 | openpose-tiny | python | - | - | - | - | - | - |  10ms | -| - |
| 图像分类 | efficientNet-B0 | python | 40ms | - | - | - | - | 80ms | - | -| - |
| 图像分类 | mobilenetv2 | rknn | - | - | - | - | - | - |  - | 120ms/rknn | - |
| 图像分类 | mobilenetv3 | python | 30ms | - | - | - | - | 100ms |  - | 48ms/ncnn | - |
| 图像分类 | Resnet50 | python | 30ms | - | - | - | - | 200ms |  - | -| - |
| 图像分类 | Resnet50 | NCNN | - | - | - | - | - | - |  2500ms | 373ms | - |
| 图像分类 | VGG-16 | RKNN | 20ms | - | - | - | - | 110ms |  - | 119ms | - |
| 图像分类 | VGG-19 | RKNN | 20ms | - | - | - | - | 170ms |  - | 117ms | - |
| 图像分类 | Xception | RKNN | - | - | - | - | - | - |  - | 130ms | - |
| 多目标跟踪 | FairMOT | python | - | - | - | 70ms | - | - | - | -| 181ms |
| 车道线检测 | LaneNet | python | - | - | - | - | - | - | - | 320ms | - |

