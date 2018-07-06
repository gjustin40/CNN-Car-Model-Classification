# Construct car model classifier with datasets which we made from various View Point Image.
- This is the project i proceeded in Univ class before.

## Goal
Implement model that can classify specific vehicle by increasing number of data through image distortion we generated.
<br>

## Datasets
- Images from sites 'google' & 'naver'
- We use only front side of cars because there are no enough images(specific models we use, not just 'car')
- Additionally, we tried two parts of car(whole part & front grill) to compare which data is the best.
- The point of our project is that image we made from various View Point image was used.
![Original Data from sites]

## Method
### 1. Machine Learning
- Extract particular feature from image and classify with Machine Learning
- We tried to use various descriptors, but It was hard to apply other descriptor for extracting features except '(Hu) Moment invariant' 
- In this case, we use 'Decision Tree' for classification model.

### 2. Deep Learning
- Trouble with selecting descriptors, we move on to Deep Learning.
- 
