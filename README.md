# - 模型性能比较


| 场景     | 模型       |参数FLOPS  | 环境    |GTX1060 | GTX1070  | GTX1080TI | GTX2080TI   | i7-9550 |i5-9400F| SOM-RK3399 | TB-RK3399Pro |GTX1650
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |:-: |:-: |:-: |
| 目标检测 | yolov3-320 |           | rknn    | /               | /         | /         | /           | /       | /     | /           | 75ms        | /     |
| 目标检测 | yolov3-416 |           | rknn    | /               | /         | /         | /           | /       | /     | /           | 90ms        | /     |
| 目标检测 | yolov3-416 |           | keras   | 100ms   | 80ms      | 60ms      | 50ms        | -       | -     | -           | -           | -     |
| 目标检测 | yolov3-416 |           | darknet | -            | -         |   -       | -           | 150ms   | -     | -           |  -          | - |
| 目标检测 | yolov3-416 |           | openvino| /         | /         | /         | /           |60ms/30ms| -     | /           | /           |  / |
| 目标检测 | yolov3-416 |           | tensorRT| /           | /         | 25ms      | /           | /       | /     | /           | /           |  65ms |
| 目标检测 | yolov3-416-fp16 |      | tensorRT        |35ms   | TODO      | TODO      | TODO        | /       | /     | /           | /           |  TODO |
| 目标检测 | yolov3-608-fp16 |      | tensorRT        |70ms   | TODO      | TODO      | TODO        | /       | /     | /           | /           |  TODO |
| 目标检测 | yolov3-tiny-416 |      | rknn                 | /     | /         | /         | /           | /       | /     |/            | 30ms        | / |
| 目标检测 | yolov3-tiny-416 |      | keras                | -     | -         | -         | -           | -       | 300ms |-            | -           | - |
| 目标检测 | yolov3-tiny-416 |5.571B|darknet  | 33ms  | -         | -         | -           | 100ms   | -     |-            | -           | - |
| 目标检测 | yolov3-tiny-608-fp16|  |tensorrt   | 11ms  | -         | -         | -           | -       | -     |-            | -           | - |
| 目标检测 | yolov4-416 |59.7B      |darknet        | 38ms  | -         | -         | -           | -       | -     |-            |   -         |  - |
| 目标检测 | yolov4-608 |           |pytorch             | 100ms | -         | -         | -           | -       | -     |-            |   -         |  - |
| 目标检测 | yolov4-608 |           |ncnn                  | -     | -         | -         | -           | 5000ms  | -     |-            |   -         |  - |
| 目标检测 | yolov4-608 |           |ncnn+vulkan| -   | -         | -         | -           | TODO    | -     |-            |   -         |  - |
| 目标检测 | yolov4-608 |128.5B     |darknet  | 70ms  | -         | -         | -           | 270ms   | -     |-            |   -         |  -|
| 目标检测 | yolov4-608-fp16 |      |tensorrt     | 90ms? | -         | -         | -           | TODO    | -     |-            |   -         |  - |
| 目标检测 | yolov4-tiny-416 |6.91  |darknet  | 33ms  | -         | -         | -           | 400ms   | -     |-            |   -         |  33ms |
| 目标检测 | yolov4-tiny-416 |      |pytorch      | 40ms  | -         | -         | -           | -       | 50ms  |-            |   -         |  - |
| 目标检测 | yolov4-tiny-416 |      |ncnn            | -     | -         | -         | -           | 180ms   | 135ms |-            | 1500ms      |  - |
| 目标检测 | yolov4-tiny-416 |      |ncnn+vulkan| -   | -         | -         | -           | TODO    | -     |-            |   -         |  - |
| 目标检测 | yolov4-pacsp-384-512|  |pytorch  | 30ms  | -         | -         | -           | -       | 350ms |-            |   -         |  - |
| 目标检测 | enetb0-yolov3|3.73B    |darknet  | 103ms | -         | -         | -           | 100ms   | -     |-            |   -         |  -|
| 目标检测 | yolov5s-640  |13.2B    | pytorch | 15ms  | -         | -         | -           | -       | 300ms |-            | -           | - |
| 目标检测 | yolov5m-640  |39.4B    | pytorch | 33ms  | -         | -         | -           | -       | -     |-            | -           | - |
| 目标检测 | yolov5l-640  |88.1B    | pytorch | 50ms  | -         | -         | -           | -       | -     |-            | -           | - |
| 目标检测 | yolov5l-640  |166.4B   | pytorch | 84ms  | -         | -         | -           | -       | -     |-            | -           | - |
| 目标检测 | mobilenetv3-ssd |      | python  | -     | -         | -         | -           | -       | -     | -           | -           | - |
| 目标检测 | faster-rcnn |                 | mmdetect| 170ms  | -         | -         | -           | -       | -     | -           | -           | - |
| 目标检测 | fovea            |                 | mmdetect| 150ms  | -         | -         | -           | -       | -     | -           | -           | - |
| 人脸识别 | deepface |             | python           |  -    |         - | -         | -           | -       | -     | -           | -           |  - |
| 人脸检测 | libfacedetect |        | c                    | -     | -         | -         | -           | 30ms    |       |  -          |  -          | - |
| 人脸检测 | yolo-face |   6.94B    | darknet   | 33ms  | -         | -         | -           | TODO    |       |  -          |  -          | - |
| 人脸检测 | dbface |               | pytorch           | -     | -         | -         | 100ms       | -       | -     | -           |  -          | - |
| 人脸检测 | retinaface-r50 |       | tensorrt    | 130ms | -         | -         | TODO        | -       | -     | -           |  -          | - |
| 人脸检测 | retinaface-RFB |       | NCNN     | -     | -         | -         | TODO        | -       | 7ms   | -           |  -          | - |
| 姿态检测 | openpose |             | python       | -     | -         | -         | -           | -       | 40ms  | -           |  -          | - |
| 姿态检测 | openpose-tiny |        | python  | -     | -         | -         | -           | -       | -     |  10ms       | -           | - |
| 图像分类 | efficientNet-B0 |      | python   | 40ms  | -         | -         | -           | -       | 80ms | -            | -           | - |
| 图像分类 | densenet-bc-L100-k12|0.02M|pytorch| -    | -         | -         | -           | -       | -     |  -          |             | - |
| 图像分类 | mobilenetv2 |          | rknn          | -     | -         | -         | -           | -       | -     |  -          | 120ms/rknn | - |
| 图像分类 | mobilenetv3 |  31M | python  | 30ms  | -         | -         | -           | -       | 100ms |  -          | 48ms/ncnn   | - |
| 图像分类 | Resnet50 |             | python       | 30ms  | -         | -         | -           | -       | 200ms |  -          | -           | - |
| 图像分类 | Resnet50 |             | NCNN         | -     | -         | -         | -           | -       | -     |  2500ms     | 373ms       |  - |
| 图像分类 | VGG-16 |               | RKNN           | 20ms  | -         | -         |  -          | -       | 110ms |  -          | 119ms       | - |
| 图像分类 | VGG-19 |               | RKNN            | 20ms  | -         | -         | -           | -       | 170ms |  -          | 117ms       | - |
| 图像分类 | Xception |             | RKNN         | -     | -         | -         | -           | -       | -     |  -          | 130ms       | - |
| 多目标跟踪 | FairMOT |            | python     | -     | -         | -         | 70ms        | -       | -     | -           | -           | 181ms |
| 车道线检测 | LaneNet |            | python     | -     | -         | -         | -           | -       | -     |  -          | 320ms       | - |
| 实例分割 | maskrcnn |        | mmdetection | 210ms | -         | -         | -           | -       | -     |  -          | -       | - |

