# HumberMachineLearning
'''
Welcome to the machine learning course!

In support of the first microlecture on machine learning. You will find the YOLOV5 model trained on detecting defects in french fries.

To enable training. Lets first learn how to set it up.
You will find two main folders.
First is the datasets folder and the second is the yolov5 folder.
All the training data has to go inside the datasets folder
The training dataset is in datasets/coco128/train/images and the labels for the images is in datasets/coco128/train/labels
To mark training data with labels one needs a tool like roboflow https://roboflow.com/ Here you can upload your training data and then eithe manually
annotate the data in images. Here it would mean manually marking the area of defect and labeling them. In our case we have four types of defects A,B,C,D

As an example you can see 255_png.rf.1926febf4295d0147693a02bb4840006.jpg in the training folder and the corresponding label file 

2 0.17890625 0.36484375 0.0046875 0.0046875

2 0.46484375 0.6625 0.0046875 0.0046875

2 0.2203125 0.65234375 0.0046875 0.0046875

1 0.50078125 0.52265625 0.02265625 0.02265625

1 0.471875 0.51796875 0.0046875 0.0046875

1 0.75234375 0.528125 0.01015625 0.009375

1 0.77578125 0.646875 0.01015625 0.009375

1 0.5125 0.7671875 0.01015625 0.009375

1 0.10625 0.571875 0.01015625 0.009375

1 0.2734375 0.53359375 0.01015625 0.009375

1 0.69375 0.7234375 0.01015625 0.009375

1 0.3375 0.7890625 0.01015625 0.009375

1 0.6296875 0.36484375 0.01015625 0.009375

1 0.478125 0.21640625 0.01015625 0.009375

1 0.6359375 0.08984375 0.0046875 0.0046875

0 0.78671875 0.2640625 0.0046875 0.0046875

0 0.4625 0.37578125 0.0046875 0.0046875

0 0.76875 0.63203125 0.0046875 0.0046875

This label file shows in first column the type of defect (0->A, 1->B, 2->C, 3->D) and the coordinates (x,y) of the pixels of two corners of the 
bounding box around them. 

YOLOv5 uses a combination of the file and the labels to know which area to learn from

Once you set up the data in this fashion, training is simple. 

'''
