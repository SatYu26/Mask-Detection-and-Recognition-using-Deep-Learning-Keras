# INTRODUCTION

To create our face mask detector, we trained a two-class model of people wearing masks and people not wearing masks.<br>

We fine-tuned MobileNetV2 on our mask/no mask dataset and obtained a classifier that is ~99% accurate.<br>

We then took this face mask classifier and applied it to both images and real-time video streams by:<br>

<ul>
Detecting faces in images/video<br>
Extracting each individual face<br>
Applying our face mask classifier<br>
</ul>

Our face mask detector is accurate, and since we used the MobileNetV2 architecture, it’s also computationally efficient, making it easier to deploy the model to embedded systems (Raspberry Pi, Google Coral, Jetosn, Nano, etc.).<br>

# Project Structure
![alt text](https://github.com/SatYu26/Mask-Detection-and-Recognition-using-Deep-Learning-Keras/blob/main/face_mask_detection_phases.png)

```
$ tree --dirsfirst --filelimit 10
.
├── dataset
│   ├── with_mask [690 entries]
│   └── without_mask [686 entries]
├── examples
│   ├── example_01.png
│   ├── example_02.png
│   └── example_03.png
├── face_detector
│   ├── deploy.prototxt
│   └── res10_300x300_ssd_iter_140000.caffemodel
├── detect_mask_image.py
├── detect_mask_video.py
├── mask_detector.model
├── plot.png
└── train_mask_detector.py

5 directories, 10 files
```
The dataset/ directory contains the data described in the “Our COVID-19 face mask detection dataset” section.<br>

Three image examples/ are provided so that you can test the static image face mask detector.<br>

We’ll be reviewing three Python scripts in this tutorial:
<ul>
<li>train_mask_detector.py: Accepts our input dataset and fine-tunes MobileNetV2 upon it to create our mask_detector.model. A training history plot.png containing accuracy/loss curves is also produced</li>
<li>detect_mask_image.py: Performs face mask detection in static images</li>
<li>detect_mask_video.py: Using your webcam, this script applies face mask detection to every frame in the stream</li>
</ul>

# RESOURCES


Pretrained Model Link:- https://drive.google.com/file/d/1BeR4ukiaS5ZU5Dq3TU9Yc51Ymo8zP_Vs/view?usp=sharing

Dataset Link:- https://drive.google.com/folderview?id=1XDte2DL2Mf_hw4NsmGst7QtYoU7sMBVG

## Acknowledgment

https://www.youtube.com/watch?v=TNZAbVNTLhA&t=6172s
