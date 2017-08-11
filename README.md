# YOLO-Object-Detection-Tensorflow
YOLO: Real-Time Object Detection using Tensorflow and easy to use

![alt text](output/000430.jpgoutput.png)
![alt text](output/000864.jpgoutput.png)
![alt text](output/001432.jpgoutput.png)
![alt text](output/003065.jpgoutput.png)
![alt text](output/003785.jpgoutput.png)

#### 1- Make sure check settings.py before start to train
```python
# remove elements that you don't want
classes_name =  ["aeroplane", "bicycle", "bird", "boat", "bottle", "bus", "car", "cat", "chair", "cow", "diningtable", "dog", "horse", "motorbike", "person", "pottedplant", "sheep", "sofa", "train", "tvmonitor"]
classes_no = [i for i in xrange(len(classes_name))]
classes_dict = dict(zip(classes_name, classes_no))

image_size = 448
cell_size = 7
box_per_cell = 2
alpha_relu = 0.2
object_scale = 2.0
no_object_scale = 1.0
class_scale = 2.0
coordinate_scale = 5.0
flipped = True

learning_rate = 0.0001
dropout = 0.5
batch_size = 3
epoch = 15000
checkpoint = 10

# For main
threshold = 0.2
IOU_threshold = 0.5
test_percentage = 0.05

# 1 for read a picture
# 2 to read from testing dataset
# 3 to read from webcam / video
output = 1
# let empty if want to capture from webcam
picture_name = ''
video_name = ''
```

#### 2- You must download VOC 2012 and put in the same folder for multibox dataset
#### 3- You need to put YOLO_small.ckpt in the same folder (optional) if you want to use pretrained model
#### 3.1- You can train your own model from scratch in train-classification folder, choose full/fast model
#### 4- you must train.py in main directory first before main.py (unless if you downloaded YOLO_small.ckpt)
#### 5- test in main
