# Face_Verification
The aim of this project was to build a Siamese network in order to verify faces.

## Dataset
The dataset that I used for this project was [Labeled Faces in the Wild Home](https://vis-www.cs.umass.edu/lfw/). I loaded this dataset from the Scikit-Learn Library. 
The dataset had 3 subsets for train, test, and validation. 
  - Shape of train set: (2200, 5828)
  - Shape of test set: (1000, 5828)
  - Shape of val set: (6000, 5828)

Because we have a pair of images in each sample, the shapes look like that. In fact, Image dimensions are $62*47$ in grayscale. Each data has a pair of images so the shape of the data must be $62 * 47 * 2 = 5828$.
<br>For better results, I decided to apply some changes in the number of subset data.

### Display Pairs of Images
![](https://github.com/alireza00bin/Face_Verification/blob/main/sample.png)

## Model
I implemented the Siamese network for this project. We have two parallel networks each of them gets one of the images and processes on them. After that, we pass the conclusion of the embedding network to the Euclidean function to calculate the distance between them.
So we have a right model and also a left model
![](https://github.com/alireza00bin/Face_Verification/blob/main/siamese.png)

## Result
My train accuracy was 1 and My val accuracy was 0.63
![](https://github.com/alireza00bin/Face_Verification/blob/main/loss.png)
### Display Test Result
![](https://github.com/alireza00bin/Face_Verification/blob/main/result.png)



