![Sample](https://github.com/kdncode/tensorFlow-react/blob/master/final.gif)
# YOLO v2

YOLO9000 is a high speed, real time detection algorithm that can detect on OVER 9000! (object categories).
[Read more](https://arxiv.org/pdf/1612.08242.pdf)

## Requirements

- Python 3.5 or 3.6. [Download here](https://www.python.org/downloads/)
- Tensorflow. [Download here](https://www.tensorflow.org/install/pip)
- OpenCV [Download here](https://pypi.org/project/opencv-python/)

```bash
pip install opencv-python
```

## Download Darkflow repo

- [Download ZIP](https://github.com/thtrieu/darkflow)
- Extract.

## Build the library
- Cd to ```darkflow-master``` folder that just extracted.
- Open terminal & Run:

```bash
python setup.py build_ext --inplace
```
or
```bash
pip install -e .
```

## Download the 'weights' file
- Create ```bin``` folder inside ```darkflow-master``` folder.
- Download the YOLOv2 608x608 weights file [here](https://pjreddie.com/darknet/yolov2/).
- Put the ```weights``` file inside ```bin``` folder.

## Processing video file
- Put the video into ```darkflow-master``` folder.
- Open terminal & Run:
- Without GPU version of tensorflow:
```bash
python flow --model cfg/yolo.cfg --load bin/yolov2.weights --demo video_file_name.mp4 --saveVideo
```
- GPU version of tensorflow:
```bash
python flow --model cfg/yolo.cfg --load bin/yolov2.weights --demo video_file_name.mp4 --gpu 1.0 --saveVideo
```
*NOTE: 
- video_file_name.mp4 changes to your video name.

- --saveVideo indicates to save a name video file, which has the boxes around objects
## License
[Darkflow](https://github.com/thtrieu/darkflow/blob/master/README.md)

[Video credit](https://www.youtube.com/watch?v=tC7EucOFRok)

[Photo credit](https://unsplash.com/)
