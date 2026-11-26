# Computer Vision

The [standalone Computer Vision repository](https://github.com/HRtech-lab/Computer-Vision) contains this course and its additional runnable examples.

The image labs begin with boundaries and gradient descriptors, then use a convolutional network for classification and a U-Net for binary segmentation. The video labs follow motion from frame to frame and then classify short clips.

| Track | Examples | What the output measures |
| --- | --- | --- |
| [Images](Images/README.md) | Canny edges, HOG with a linear SVM, a convolutional digit classifier and U-Net segmentation | Boundary precision and recall, class-wise prediction errors, intersection over union and Dice overlap. |
| [Videos](Videos/README.md) | Lucas-Kanade tracking, Farnebäck flow, background subtraction and a 3D convolutional classifier | Endpoint error in pixels, the fraction of valid tracks, foreground overlap and motion-class accuracy. |

## Two examples

A noisy shape has a known outline, so its detected edges can be scored against a boundary with a fixed pixel tolerance. In the tracking lab the scene moves by a known translation, so every proposed displacement has a reference value. Both scenes can be regenerated offline. [Edge detection](Images/01%20Canny%20Edge%20Detection/README.md) · [Sparse tracking](Videos/01%20Lucas-Kanade%20Tracking/README.md)

![Reference geometry and detected edges](Images/01%20Canny%20Edge%20Detection/figure.svg)

## Run a lab

Use Python 3.12. Install the dependencies from this folder, then run a script or open the corresponding notebook. Keep the `gallery` folder with the course when downloading it.

```sh
python -m pip install -r requirements.txt
python "Videos/01 Lucas-Kanade Tracking/lucas_kanade_tracking.py"
```

Optical digit recognition uses the 8 × 8 UCI images supplied with scikit-learn and an image-level split. The other scenes and video clips are generated locally. Each example cites the method and describes its evaluation. [UCI optical digits](https://doi.org/10.24432/C50P49) · [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) · [MIT code licence](../LICENSE)
