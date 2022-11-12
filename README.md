# HumberMachineLearning
'''
Welcome to the machine learning course!

In support of the first microlecture on machine learning. You will find the YOLOV5 model trained on detecting defects in french fries.

To make this happen you should have several python APIs installed on your computer.

to do that, go to yolov5 folder and see the requirements.txt

to install all the prerequisites execute the following command

pip3 install -r requirements.txt

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

go to the yolov5 folder and execute the following command from command prompt

python3 train.py --data coco128.yaml --weights yolov5s.pt --img 640  # from pretrained (recommended)

If you have python installed as python3 you can use only python on it.

This training will take a significant amount of time. On a mac 16 inch it took 1.5 days so be ready on your laptop. So dont worry if you take some time.
Also turn off your computers auto shut down features. (keep it shut for the duration of this course), you will be training and testing a lot of systems.

Now once the model is trained and ready put the best.pt into the weights folder of yolov5. The best.pt would be found in the runs\exp<no>\weights folder. Copy paste it into weights folder of the yolov5 base folder (yolov5\weights). 

Now to test the model, you can put the test images into yolov5\data\images folder. 

Use this command from the yolov5 folder to now pass all the images in the yolov5\data\images folder through classification of errors. 
python3 detect.py --weights weights/best.pt --source data/images

This command will put all the tested images into runs\detect\exp<no> folder. you can see the results

Now through this class you will get to play with this model and set it even more correctly. But today it is a handson approach to get started,\

As a follow up, read about YOLOV5 model and what it can and cannot do! You can comment on it in the class blog. 
  
Happy Learning!



'''
