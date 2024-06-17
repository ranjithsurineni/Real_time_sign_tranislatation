# Real_time_sign_tranislatation


REAL TIME LANGUAGE ASSISTANT FOR SIGN TRANSLATION

****ABSTRACT****


Sign language is one of the oldest
and most natural form of language
for communication, but since most
people do not know sign language
and interpreters are very difficult to
come by, we have come up with a
real time method using neural
networks for fingerspelling based
on American sign language. In our
method, the hand is first passed
through a filter and after the filter is
applied the hand is passed through a
classifier which predicts the class of
the hand gestures.
With the advancements in computer
vision technology, learning and
using sign languages to
communicate with deaf and mute
people has become easier. Exciting
research is ongoing for providing a
global platform for communication
in different sign languages. In this
project, we present a Deep
Learning-based approach to
recognize a sign performed in
American Sign Language by
capturing an image as input. The
system can predict the signs of A to
Z and Hand gestures performed by
the user. By utilizing image
processing to convert RGB data to
grayscale images, an efficient
reduction is achieved in the storage
requirements and training time of
the Convolutional Neural Network.
The objective of the experiment is
to find a mix of Image Processing
and Deep Learning Architecture
with lesser complexity to deploy the
system.


**METHODOLOGY USED:**


The project entails gathering and
preprocessing images of ASL
gestures, constructing and training a
CNN model to recognize sign
language, and developing a
user-friendly GUI interface for
seamless translation interaction. The
CNN architecture is designed to
extract spatial features from ASL
images, while the GUI integrates
with the model backend to facilitate
real-time translation and ensure an
intuitive user experience. Through
iterative refinement and
optimization, the system aims to
accurately interpret ASL gestures
and enhance accessibility for users.


![sign to speech](https://github.com/ranjithsurineni/Real_time_sign_tranislatation/assets/118590392/4aa16e9e-76a3-4859-ad0d-a72a4ed31df7)



**Getting the Dataset:**


Datasets of predefined sign language was taken from Kaggle. It had approximately 87,000
images which are 200X200 pixels belonging to 29 classes of which 26 are for the letters A-Z
and 3 classes for SPACE, DELETE and NOTHING. These 3 classes are very helpful in
real-time applications, and classification.corresponding to each alphabet including both
training and test data sets.


![sample_dataset](https://github.com/ranjithsurineni/Real_time_sign_tranislatation/assets/118590392/082ed099-6848-49a9-bcc6-86bdb0076508)


**Data Pre-Processing:**


The training data of the sign images was taken and was cleaned to make it ready for
classification. All the images were appended to an image array. The image array was then
converted to a numpy array. The array was normalized by converting the values to ‘float32’
and dividing it with the total sum of the pixel values i.e. 255. The labels corresponding to each
image was stored in a array as well and was converted to categorical values using the internal
function present in keras module. The whole image data was split into training and testing
using the internal function present in scikit-learn module. The shape of the train and test data
was printed and returned back for the model to consume


****Dataset Splitting:****


30% of the dataset is reserved for testing, while the
remaining 70% is allocated for training. 


**Building Convolutional model:**

![Screenshot (19)](https://github.com/ranjithsurineni/Real_time_sign_tranislatation/assets/118590392/2ab587fa-21fd-4114-a0f1-975727d5f76e)

CNN_model_summary

**Model Evaluation:**

![Screenshot (1)](https://github.com/ranjithsurineni/Real_time_sign_tranislatation/assets/118590392/e9b2b0c9-e259-4aa2-aaf8-735e87592432)


**Creating a GUI using Tkinter:**

**Tkinter** is a Python library that serves as the standard GUI (Graphical User Interface) toolkit
for Python. It allows developers to create desktop applications with graphical interfaces in a
straightforward and efficient manner. Tkinter is included with most Python installations,
making it readily available for development without the need for additional installations.

**Enchant** used in Suggestion Generation, Grammar Checking and Correction, Spellchecking
Across Languages, Customization and Extensibility, Integration with Python Ecosystem.
We created a graphical user interface (GUI) application using the Tkinter library for sign
language classification and text-to-speech conversion.
**Importing Libraries**: The begins by importing necessary libraries, including Tkinter, PIL
(Python Imaging Library) for image processing, OpenCV (cv2) for computer vision tasks, and
pyttsx3 for text-to-speech conversion.
**Loading Pre-trained Model**: It loads a pre-trained deep learning model (`model.h5`) for sign
language classification using Keras.


**Defining Functions:**
- `sign_to_text`: Converts sign language frames to text using the loaded model.
- `text_to_speech`: Converts text to speech using the text-to-speech engine.
- `start_video_feed` and `stop_video_feed`: Functions to start and stop the video feed from
the webcam.
- `clear_text`: Clears the predicted text.
- `convert_text_to_speech`: Reads text from the textbox and converts it to speech.


![Screenshot (229)](https://github.com/ranjithsurineni/Real_time_sign_tranislatation/assets/118590392/e4f188da-4c98-4393-a502-69cb7f94bff3)


**RESULTS AND ANALYSIS**


Our proposed methodology‘s execution has been examined on the test data which was distinct
from the training data set. The testing process involves 87,000 image samples of different
hand signals. All these images were simultaneously updated into our proposed model to come
up with accurate results. Our expected result is to obtain a text which is the translation of the
sign language given as an input. Our model will anticipate all the hand gestures of the
American Sign Language. To achieve an efficient result. The estimated accuracy of our
proposed system is more than 95% even in a multiplex lighting environment which is
considered an adequate result as of now for real-time interpretation. The entire model pipeline
is developed by CNN architecture for the classification of 29 classes which 26 are for the
letters A-Z and 3 classes for SPACE, DELETE and NOTHING. The proposed work has
achieved an efficiency of 99.88%. 

**Accuracy/Loss Training Plot**

![Screenshot (22)](https://github.com/ranjithsurineni/Real_time_sign_tranislatation/assets/118590392/1b181893-7ade-423a-a416-d3d373353489)


Fig: Loss plot of the model throughout the training journey.

![Screenshot (23)](https://github.com/ranjithsurineni/Real_time_sign_tranislatation/assets/118590392/f73d9ae8-8603-4fae-8159-b0202afc05d4)


Fig: Accuracy plot of the model throughout it's training journey


**OUTPUT:**


![Screenshot (4)](https://github.com/ranjithsurineni/Real_time_sign_tranislatation/assets/118590392/3bb60ac0-9732-43c4-b9e8-95aab5209844)
![Screenshot (3)](https://github.com/ranjithsurineni/Real_time_sign_tranislatation/assets/118590392/61dca69c-086e-4398-a8ca-911574f8f33d)
