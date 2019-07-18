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

#### DATA
The first step to the project was to build a facial recognition model.
Our team of 4 took around 12 headshots of each other making different faces at the camera providing me with 48 unique pictures to work with as training data.

<img src=https://github.com/ichiu9/Research-Image-Classification-Face-And-Limbs/blob/master/Images/IMG_6520.jpg width=45% hspace="10"><img src=https://github.com/ichiu9/Research-Image-Classification-Face-And-Limbs/blob/master/Images/IMG_6525.jpg width=45% hspace="10">

#### PROCESS
I prepared the 48 png files by converting them into recordio files based on class and person. Within the recordio file, I separated the data, 70% dedicated to training, and the other 30% to validation. From there, I finetuned the hyperparameters for the model and utilized Sagemaker's image classification algorithm to build out a classification model.

#### RESULTS

The model proved to be fairly accurate providing +95% accuracy for the two of the team members and 55-65% accuracy for the other team members. These results proved that the model was functioning which meant it was time to move on to the next step of classifying limb movement from optical flow images.

### LIMB MOVEMENT RECOGNITION


#### DATA
In this second phase, our team took 4 videos of each person moving each of their arms and legs. From these 16 videos, another teammate converted the videos into optical flow images of frames.

<img src=https://github.com/ichiu9/Research-Image-Classification-Face-And-Limbs/blob/master/Images/Screen%20Shot%202019-07-17%20at%202.03.59%20PM.png width=24% height=250 hspace="2"><img src=https://github.com/ichiu9/Research-Image-Classification-Face-And-Limbs/blob/master/Images/IsaiahLeftArm_DOF_133c.png width=24% height=250 hspace="2"><img src=https://github.com/ichiu9/Research-Image-Classification-Face-And-Limbs/blob/master/Images/Screen%20Shot%202019-07-17%20at%202.04.35%20PM.png width=24% height=250 hspace="2"><img src=https://github.com/ichiu9/Research-Image-Classification-Face-And-Limbs/blob/master/Images/IsaiahRightLeg_DOF_014.png width=24% height=250 hspace="2">

#### PROCESS
After the optical flow images were created there came out to be around 2,500 images total that I was able to use for training. I spent a lot more time on the data preparation side this time around because I wanted to eventually evaluate the model using K-fold Cross Validation. This meant building 4 different sets of recordio files, each one omitting a different team member. After the data was finally prepared, I ran the model 4 different times for each set of data on a similar image classification model to the one I built for the facial recognition.

#### RESULT

<img src=https://github.com/ichiu9/Research-Image-Classification-Face-And-Limbs/blob/master/Images/i_plot.png width=50%><img src=https://github.com/ichiu9/Research-Image-Classification-Face-And-Limbs/blob/master/Images/k_plot.png width=50%><img src=https://github.com/ichiu9/Research-Image-Classification-Face-And-Limbs/blob/master/Images/r_plot.png width=50%><img src=https://github.com/ichiu9/Research-Image-Classification-Face-And-Limbs/blob/master/Images/p_plot.png width=50%>
