# Determining Chess Game State From an Image Using Machine Learning

This repository contains my [master thesis](report.pdf).

More information is available in the [main repository](https://github.com/georg-wolflein/chesscog).


## Abstract
Identifying the configuration of chess pieces from an image of a chessboard is a problem in computer vision that has not yet been solved accurately.
However, it is important for helping amateur chess players improve their games by facilitating automatic computer analysis without the overhead of manually entering the pieces.
Current approaches are limited by the lack of large datasets and are not designed to adapt to unseen chess sets.
This project puts forth a new dataset synthesised from a 3D model that is two orders of magnitude larger than existing ones.
Trained on this dataset, a novel end-to-end chess recognition system is presented that combines traditional computer vision techniques with deep learning.
It localises the chessboard using a RANSAC-based algorithm that computes a projective transformation of the board onto a regular grid.
Using two convolutional neural networks, it then predicts an occupancy mask for the squares in the warped image and finally classifies the pieces.
The described system achieves an error rate of 0.23% per square on the test set, 28 times better than the current state of the art.
Further, a one-shot transfer learning approach is developed that is able to adapt the inference system to a previously unseen chess set using just two photos of the starting position, obtaining a per-square accuracy of 99.83% on images of that new chess set.
Inference takes less than half a second on a GPU and about two seconds on a CPU.
The feasibility of the system is demonstrated in an interactive web app available at https://www.chesscog.com.
