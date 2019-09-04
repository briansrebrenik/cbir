# A Content Based Image Retrieval System for Liquor Bottles
![matches](https://github.com/briansrebrenik/cbir/blob/master/example.png)

## ORB
A CBIR system uses the content of an image, such as colors, shapes, and textures,
to search for the most similar image in a database.
In order to find the closest match, the system must use an algorithm to efficiently
find key "descriptors" for an image that can be used to compare to the descriptors
of images in the database.
For my system, I used ORB from the [OpenCV](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_feature2d/py_orb/py_orb.html) Python library.
ORB is "a good alternative to SIFT and SURF in computation cost".
