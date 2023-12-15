# IE643_Programming_Challenge_fall_2023
This is a programming challenge for an object detection task as a part of the IE643 course. 

Dataset Description
In this competition, you are tasked to detect objects present in images inside the images folder. The images folder contains both training and testing set images. Annotations for training images in the train.csv file. You have to predict box annotation and class labels for images in test.csv. A sample_submission.csv file has been provided, and your submission file should follow the same format for evaluation. The images in the dataset contains following classes:
1: pedestrian
2: people
3: bicycle
4: car
5: van
6: truck
7: tricycle
8: awning-tricycle
9: bus
10: motor
11: others

Files
train.csv - the training set with image IDs and annotations
test.csv - the test set with image IDs, you have to predict annotations for these images.
sample_submission.csv - a sample submission file in the correct format
Columns
id - unique ID related to each sample. This also corresponds to all unique images inside the image folder. Images can be accessed as images/{id}.jpg where {id} corresponds to unique ID.
annotations - this contains bounding box and class label information for each object in image {id}.jpg
The annotation string should be of the format:
[bndbox-left],[bndbox-top],[bndbox-width],[bndbox-height],[confidence],[object-label]

[bndbox-left]: The x coordinate of the top-left corner of the predicted bounding box
[bndbox-top]: The y coordinate of the top-left corner of the predicted object bounding box
[bndbox-width]: The width in pixels of the predicted object bounding box
[bndbox-height]: The height in pixels of the predicted object bounding box
[confidence]: The confidence of the predicted bounding box enclosing an object instance.
[object-label]: The object category indicates the type of annotated object.
Multiple object annotations in an image should be separated by | (pipe) symbol.
An example with three objects in the image can be:
820,679,58,108,0.5,van|1248,718,64,69,0.5,van|1296,606,68,82,0.5,van

If your model detects no objects in an image, then you can use either " " (space) or "Null" string in the submission file as annotations.
