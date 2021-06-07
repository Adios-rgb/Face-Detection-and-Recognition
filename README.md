# Face-Detection-and-Recognition
The code detects the face, recognizes it and tags it with the recognized name.

# Functionality

* Used to detect face from the image using pre-trained model.
* Recognize/classify the detected face.
* Tag the face with the recognized/classification along with the predicted probability.


![image](https://user-images.githubusercontent.com/59373491/121057002-72577980-c7dc-11eb-9fc4-972e645bbe3a.png)

# Packages used

* imutils
* OpenCV
* pickle
* os
* sklearn
* keras

# Steps Involved

• generate_images() method uses ImageDataGenerator to generate augmented images to increase the training size for each class.

• calc_and_pickle_embeddings() is used to extract faces from each of the images from all the folders, finds facial embeddings from all images and stores the flattened embeddings
along with the name. The data is stored as pickle on local storage.

• pickle_model() method loads the data from the pickle and trains RandomForestClassifier on the facial embeddings. The model is then stored as pickle.

• The driver code is used to accept data as frames and detects faces from the frame, uses our trained RandomForestClassifier to recognize/classify the face.

• Creates a bounding box on the face along with the recognized/classified name.
