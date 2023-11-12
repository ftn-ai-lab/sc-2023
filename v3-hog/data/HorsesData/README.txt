
INRIA Horses: a dataset for testing object class detection algorithms
=====================================================================

Version: 1.01


Introduction
~~~~~~~~~~~~
This dataset contains 170 images containing one or more horses horses collected from the Internet (positive images), and 170 images without horses (negative images).
The main challenges it offers are clutter, intra-class shape variability, and scale changes.
The horses are mostly unoccluded, taken from approximately the side viewpoint, and face the same direction.

The dataset has been collected and annotated by Vittorio Ferrari and Frederic Jurie.
Experiments on it appeared in

V. Ferrari, F. Jurie, and C. Schmid,
Accurate Object Detection with Deformable Shape Models Learnt from Images,
CVPR 2007, Minneapolis, USA

V. Ferrari, L. Fevrier, F. Jurie, and C. Schmid,
Groups of Adjacent Contour Segments for Object Detection,
IEEE Transactions on Pattern Analysis and Machine Intelligence, January 2008

V. Ferrari, F. Jurie, and C. Schmid
From Images to Shape Models for Object Detection
International Journal of Computer Vision, accepted (to appear), 2009.



Groundtruth
~~~~~~~~~~~
Object annotations are included in files

<image>_entires.groundtruth

Each line in the file encodes the bounding-box of a horse in <image>

The coordinates of the bounding-box appear in the following format

top_left_x  top_left_y  bottom_right_x  bottom_right_y



Edgemaps
~~~~~~~~
In files *_BSE/*.pgm, we include edgemaps produced by the excellent Berkeley 'natural boundary detector'.
We recommend using this advanced edge detector instead of the standard Canny (http://www.eecs.berkeley.edu/Research/Projects/CS/vision/grouping/segbench/).


Contact
~~~~~~~
If you have a question please contact

Vittorio Ferrari (ferrari@vision.ee.ethz.ch)

We would be glad to know about your results on this dataset !



Updates
~~~~~~~
New in version 1.01:
- this README.txt
- packaged in a single .tgz
- only include the official 170 negative images belonging to this dataset (version 1.00 included 700+ negative images)
- all images in the *BSE directories have the same filename has the corresponding raw images (no more empty spaces as in version 1.00)
