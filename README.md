# Research Image Classification Face And Limbs

## Classifying teammates from a research group and limb movements from the arms and legs.

This Project contains 2 Sub-goal / Milestones that I was responsible for in this research project:
- https://github.com/kryan225/Research---Cerebral-Palsy-Detection
  
### OVERVIEW

#### GOAL
The purpose of this project is to understand the image classication capabilities that AWS Sagemaker provides.
Once a deeper level of understanding is reached, my team will decide if Sagemaker should be utilized and if the same hyperparameters should be used when dealing with baby accelerometer data.

Ultimately, once an image classification model is completed and is proved to have a reliable accuracy, the same concepts and model will be moved to the nicu data to predict signs of cerebral palsy in premature babies

### FACIAL RECOGNITION

#### PROCESS
The first step to the project was to build a facial recognition model.
Our team of 4 took around 12 headshots of each other making different faces at the camera providing me with 48 unique pictures to work with as training data.

<img src=https://github.com/ichiu9/Research-Image-Classification-Face-And-Limbs/blob/master/IMG_6520.jpg width=50%><img src=https://github.com/ichiu9/Research-Image-Classification-Face-And-Limbs/blob/master/IMG_6525.jpg width=50%>

I prepared the 48 png files by converting them into recordio files based on class and person. Within the recordio file, I separated the data, 70% dedicated to training, and the other 30% to validation. From there, I finetuned the hyperparameters for the model and utilized Sagemaker's image classification algorithm to build out a classification model.

#### RESULTS

The model proved to be fairly accurate providing +95% accuracy for the two of the team members and 55-65% accuracy for the other team members. These results proved that the model was functioning which meant it was time to move on to the next step of classifying limb movement from optical flow images.

### LIMB MOVEMENT RECOGNITION


#### PROCESS
In this second phase, our team took 4 videos of each person moving each of their arms and legs. From these 16 videos, another teammate converted the videos into optical flow images of frames.
