# Construct car model classifier with datasets which we made from various View Point Image.
This is the project i proceeded in Univ class before.

## Goal
Implement model that can classify specific vehicle by increasing number of data through image distortion we generated.
<br>

## Datasets
- Images from sites 'google' & 'naver'
- We used only front side of cars because there are no enough images(specific models we use, not just 'car')
- Additionally, we tried two parts of car(whole part & front grill) to compare which data is the best.
- The point of our project is that image we made from Various View Point image was used.
- We used 3 classes(Audi, Benz, Grandeur), Each class has 250 image(train : 200, test : 50).
- Although we have a few image, we want to try using Keras
![Original Data from sites]


### Various View Point Image(increasing number of images)
1. Get the front grilles(& whole images) from vehicle images which is clear and have no noise.
2. Distortion these image just like side view of the vehicles using control points of image.
(Only front part of the car)
3. Set a degree of viewpoint depending on how many images you want to generate.
4. Save those distorted images for the dataset.
5. Repeat 1~4 on each class(3 classes(models) in my case)

## Method
### 1. Machine Learning
- Extract particular feature from image and classify with Machine Learning
- We tried to use various descriptors, but It was hard to apply other descriptor for extracting features except '(Hu) Moment invariant' 
- In this case, we use 'Random Forest' for classification model.
- This method need specific image.<br>
> Convert RGB to grayscale and make it to binary image to apply 'hu moment' function.<br>
(background should be black and grill should be white to get the shape parameter of it from 'hu moment' function)
- Unfortunately, This method have failed. The reason was that image sizes were too big to train with 'Decision Tree'.
- Furthermore, It was hard to select adequate descriptor for our high level images.

### 2. Deep Learning
- Trouble with selecting descriptors, we moved on to Deep Learning, CNN.
- We chose 'Keras' for CNN tools because it Allows for easy and fast prototyping. <a href = 'https://keras.io/'>Keras Documentation</a>
- In addition, we made CNN model suitable for our datasets by changing the size of various hidden layer structures and filters.
<hr>
Sorry for the English.
