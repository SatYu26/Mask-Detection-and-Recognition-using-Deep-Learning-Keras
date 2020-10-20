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

# RESOURCES


Pretrained Model Link:- https://drive.google.com/file/d/1BeR4ukiaS5ZU5Dq3TU9Yc51Ymo8zP_Vs/view?usp=sharing

Dataset Link:- https://drive.google.com/folderview?id=1XDte2DL2Mf_hw4NsmGst7QtYoU7sMBVG
