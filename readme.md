# Project Name Northeast-American-Backyard-Bird-Identifier

 Add short description of project here > 
The AI identifies 5 of the most common types of backyard birds in the northeastern U.S using image classification.  The five types of birds that can be identified are American Robin, Blue Jay, Male Northern Cardinal, Mourning Dove, and Red Winged Blackbird.  This project, which identifies the type of backyard bird on an image, can be educational for children and be helpful for bird watchers who are looking for specific types of birds that visit backyards in the region.


![add image descrition here](direct image link here)
![add image descrition here](https://github.com/Sonicbluespeed/Northeast-American-Backyard-Bird-Identifier-Jetson-Nano/blob/master/Blue_Jay_bird_detection)

## The Algorithm

Add an explanation of the algorithm and how it works. Make sure to include details about how the code works, what it depends on, and any other relevant info. Add images or other descriptions for your project here. 
This project was developed on Jetson Nano.  The backyard bird image data set was intially obtained from kaggle.  The original set, which contained 16 bird types, was reduced to 5 bird types in order to decrease the time for training the model. Since the original data set contained corrupt images which caused the training the fail, the corrupt images were filtered and deleted. My training set had between 120 to 250 images per classification.  The validiation set contained between 30 to 70 images and the testing set had around 30 images per classification.   

I began by training my model with 5 epochs and increased it by intervals of 10 epochs up to 40.  The accuracy of the image classification probability increased from around 26% to 83%.  The final trained resnet18 model uses the imagenet.py program to classify new backyard bird images.

## Running this project

1. Add steps for running this project.
2. Make sure to include any required libraries that need to be installed for your project to run.
Download this project's resnet18.onnx, test, and labels.txt into the jetson nano
Clone the jetson-inference project in github using (https://github.com/dusty-nv/jetson-inference)


[View a video explanation here](video link)
