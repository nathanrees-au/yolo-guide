# YOLO-GUIDE
YOLO-GUIDE is a custom-trained object detection and classification model, based on the YOLOv7 algorithm. The custom dataset was collected from the [COCO 2017 Train images](https://cocodataset.org/#download) dataset. The model has been trained to identify the following 10 classes of objects:

* bed
* cell phone
* chair
* couch
* dining table
* dog
* laptop
* person
* potted plant
* television

View the publication based on our work here:
[Robotic Guide Dog for Real-time Indoor Object Detection and Classification with Localization](https://doi.org/10.1109/apscon60364.2024.10465953)

## YOLOv7 Setup

Follow the steps outlined in the official [YOLOv7 repository](https://github.com/WongKinYiu/yolov7).

## Download the Custom YOLO-GUIDE Weights

Download the `yolo-guide.pt` file and save to your cloned YOLOv7 directory.

## Run Inference

Run the standard YOLOv7 inference command with desired parameters, but specify the weights as `--weights yolo-guide.pt`:

```python
python detect.py --weights yolo-guide.pt --source 0
```

## Additional Support

### Fine-tune Parameters
To adjust more parameters for inference, download the `detect-yolo-guide.py` file and adjust your desired parameters. Use this script when running the inference instead of `detect.py`.

### Change Video Source
To change the video source the inference will be run on, specific the source as `--source yourvideo.mp4`:

```python
python detect.py --weights yolo-guide.pt --source yourvideo.mp4
```

### Adjust Confidence Threshold
The default confidence threshold is 0.25. To adjust the threshold of classified (and displayed) objects, specify the confidence threshold as `--conf-thres 0.4`:

```python
python detect.py --weights yolo-guide.pt --source 0 --conf-thres 0.4
```

## Acknowledgment

* [YOLOv7](https://github.com/WongKinYiu/yolov7)
* [UTS Robotics Institute](https://www.uts.edu.au/research/robotics-institute)
