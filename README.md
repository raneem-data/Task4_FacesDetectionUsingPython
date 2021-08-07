# Task4_FacesDetectionUsingPython
Faces Detection Using Python and downloding opencv2 

steps followed:

1-download open cv2 in pycharm(picture in file below of downloding) 


2-start write code and the code is the following:

import cv2
import sys

imagePath = sys.argv[0]
cascPath = "haarcascade_frontalface_default.xml"

faceCascade = cv2.CascadeClassifier('/Users/RaneemBeast/Downloads/haarcascade_frontalface_default.xml')

image = cv2.imread('/Users/RaneemBeast/Downloads/people-persons-peoples.jpg')
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

faces = faceCascade.detectMultiScale(
    gray,
    scaleFactor=1.1,
    minNeighbors=5,
    minSize=(30, 30),
    #flags = cv2.cv.CV_HAAR_SCALE_IMAGE
)

print("Found {0} faces!".format(len(faces)))

# Draw a rectangle around the faces
for (x, y, w, h) in faces:
    cv2.rectangle(image, (x, y), (x+w, y+h), (0, 255, 0), 2)

cv2.imshow("Faces found", image)
cv2.waitKey(0)


done with code


3- run the code and the faces are found and program point to them, all pictures results in the file bellow 

[Task4_raneemmuk.pdf](https://github.com/raneem-data/Task4_FacesDetectionUsingPython/files/6948364/Task4_raneemmuk.pdf)
