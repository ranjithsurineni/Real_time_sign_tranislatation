# Real_time_sign_tranislatation
#REAL TIME LANGUAGE ASSISTANT FOR SIGN TRANSLATION

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


**METHODOLOGY USED**


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

** Data Pre-Processing**


The training data of the sign images was taken and was cleaned to make it ready for
classification. All the images were appended to an image array. The image array was then
converted to a numpy array. The array was normalized by converting the values to ‘float32’
and dividing it with the total sum of the pixel values i.e. 255. The labels corresponding to each
image was stored in a array as well and was converted to categorical values using the internal
function present in keras module. The whole image data was split into training and testing
using the internal function present in scikit-learn module. The shape of the train and test data
was printed and returned back for the model to consume


** Dataset Splitting**


30% of the dataset is reserved for testing, while the
remaining 70% is allocated for training. 
