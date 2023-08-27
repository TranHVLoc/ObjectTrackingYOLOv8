# ObjectTrackingYOLOv8 for Self-driving Cars
This is an object tracking Computer Vision model to track cars and truck on the road using YOLOv8, ByteTrack, and SuperVision

## Object Detection with YOLOv8
YOLO (You Only Look Once) is primarily designed for object detection tasks, which involve identifying and localizing objects within an image. As technology always improves everyday. YOLOv8 is the most accurate and fastest.

### What is YOLOv8?
YOLOv8 is a new state-of-the-art computer vision model from Ultralytics. The Ultralytics package has the `yolo` class, that is used to create the Neural Network model. The YOLOv8 model contains out-of-the-box support for object detection, classification, and segmentation tasks, accessible through a Python package as well as a command line interface. Basically, it is a group of CNN models created and trained using PyTorch framework, whose package provides a single python API to work with.

YOLOv8 is an anchor-free model. This means it predicts directly the center of an object instead of the offset from a known anchor box.

### Install YOLOv8:
    pip install ultralytics


YOLOv8 provides an SDK that allows training or prediction in just a few lines of Python code.

```
from ultralytics import YOLO

# load model
model = YOLO(MODEL_PATH)
model.fuse()

# predict
detections = model(frame)
```


This project uses two basic features — model loading and inference on a single image. In the example above, MODEL_PATH is the path leading to the model. For pre-trained models, we can simply define the version of the model you want to use, for example, `yolov8x.pt`. And a frame is an `numpy` array representing a loaded photo or frame from a video.

## Object Tracking with ByteTrack
In order to count how many individual objects have crossed a line, we need a tracker. And it is **ByteTrack**

    pip install bytetracker

## Result

This is original video:

<video src="./Busy_Streets.mp4" controls="controls" style="max-width: 730px;"></video>

This is the result:

[Click here to view the video](./Busy_Streets-result.mp4)
