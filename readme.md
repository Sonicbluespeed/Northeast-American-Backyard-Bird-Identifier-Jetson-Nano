# Project Name Northeast-American-Backyard-Bird-Identifier

The five types of birds that can be identified are American Robin, Blue Jay, Male Northern Cardinal, Mourning Dove, and Red Winged Blackbird.  This project, which identifies the type of backyard bird on an image, can be educational for children and be helpful for bird watchers who are looking for specific types of birds that visit backyards in the region.

Sample output file that classifies a Blue Jay

![sample output file that classifies a Blue Jay](https://github.com/Sonicbluespeed/Northeast-American-Backyard-Bird-Identifier-Jetson-Nano/blob/master/Blue_Jay_bird_detection)

## The Algorithm

This project was developed on Jetson Nano.  The backyard bird image data set was intially obtained from kaggle.  The original set, which contained 16 bird types, was reduced to 5 bird types in order to decrease the time for training the model. Since the original data set contained corrupt images which caused the training to fail, the corrupt images were filtered and deleted. My training set had between 120 to 250 images per classification.  The validiation set contained between 30 to 70 images and the testing set had around 30 images per classification.   

I began by training my model with 5 epochs and increased it by intervals of 10 epochs up to 40.  The accuracy of the image classification probability increased from around 26% to 83%.  The final trained resnet18 model uses the imagenet.py program to classify new backyard bird images.

## Running this project

1. Clone the jetson-inference project in github using the command: git clone --recursive https://github.com/dusty-nv/jetson-inference

2. Make sure that the python packages are installed with the command: sudo apt-get install libpython3-dev python3-numpy

3. Download this project into the Jetson Nano with 
wget https://github.com/Sonicbluespeed/Northeast-American-Backyard-Bird-Identifier-Jetson-Nano/archive/refs/heads/master.zip

4. Unzip the project using the command: unzip master.zip

5. Change to the project directory using the command: cd Northeast-American-Backyard-Bird-Identifier-Jetson-Nano-master/

6. Classify a bird image using the command:
imagenet.py --model=./resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=labels.txt test/Blue\ Jay/dncygwtjva.jpg bird.jpg

The model parameter points to the trained model from the project directory.  The labels parameter points to the labels file from the project directory.  The path to a test image in the test directory is given.  The output will be in the bird.jpg in the current directory.

[View a video explanation here](video link)
