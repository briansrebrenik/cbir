# A Content Based Image Retrieval System for Liquor Bottles
![matches](https://github.com/briansrebrenik/cbir/blob/master/example.png)

## ORB
A CBIR system uses the content of an image, such as colors, shapes, and textures,
to search for the most similar image in a database.
In order to find the closest match, the system must use an algorithm to efficiently
find key "descriptors" for an image that can be used to compare to the descriptors
of images in the database.
For my system, I used ORB (Oriented FAST and Rotated BRIEF) from the [OpenCV](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_feature2d/py_orb/py_orb.html) Python library.
ORB is "a good alternative to SIFT and SURF in computation cost".
ORB combines the [FAST](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_feature2d/py_fast/py_fast.html) algorithm for corner detection and the [BRIEF](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_feature2d/py_brief/py_brief.html)
algorithm for feature descriptor calculation, "with many modifications to enhance
performance".

## Feature Matching
After calculating descriptors for all of the reference images, in order to run
the system, we must first calculate the descriptors for the query image, and then
use an algorithm to find the closest matching image in the database (reference
  images). For this I used a [Brute Force Matcher](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_feature2d/py_matcher/py_matcher.html#).
  The Brute Force Matcher, a type of nearest neighbors algorithm, that takes the
  descriptors of the query image and matches with the reference images using a
  distance calculation. For my algorithm, I used the top 10 matches for each image,
  and then chose a best match using the lowest average distance.

## How to use the CBIR
The "orb.py" file contains all of the functions required to read in the images,
calculate descriptors, and then run the brute force algorithm to find the closes match.
I ran the algorithm over all the query images, and the results can be found in the
image retrieval tests Jupyter Notebook (I have also included a pdf if you have
  difficulty opening the notebook).

## Outlined Steps:
Below I outline the steps I took in the notebook referenced above:

1. 
