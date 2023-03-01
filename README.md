# Unstructured Point Cloud Normal Estimation Using Deep Learning

<img width="394" alt="image" src="https://user-images.githubusercontent.com/22410337/222209969-33f01806-4bab-48ec-a9bf-8c88f89fdd55.png">

*The model estimates for the normals of a synthetically generated pyramid. In this test example the pyramid point cloud is noisy and the CNN still has accurate results*

# Problem Statement

Many point cloud processing applications have a better performance when the normals for the point cloud are correctly estimated. Normal estimation is the process of predicting the normal for each point in the cloud. This process is easy on flat surfaces but can be harder on noisy data and surfaces with sharp features and point density variations. Data captured with LiDAR, photogrammetry or other point cloud capturing techniques are usually noisy, present a lot of sharp features and have sample density variations.
Boulch and Marlet present a new method for normal estimation that tries to address all these problems on surfaces with sharp edges in their work "Alexandre Boulch and Renaud Marlet “Deep learning for robust normal esti- mation in unstructured point clouds”. In: Computer Graphics Forum. Vol. 35. 5. Wiley Online Library. 2016, pp. 281–290."

**The code in this repository is an implementation of their work.**

# Paper Summary

The method includes a randomised Hough Transform that is created for each point and a Convolutional Neural Network that learns the function that maps the Hough Accumulator to its normal. Generally, the process can break down to several steps. First there is the Hough Transformation that transforms the data to Hough Space and a voting scheme to create a hough accumulator, then there’s the training data generation process to create the training samples for the network to learn, and finally, there’s the Convolutional Neural Network architecture along with the training algorithm.

# Run the code

It is strongly encouraged to run the notebook
in google colab using the link below:

https://colab.research.google.com/drive/17GuMRSDZRqLGLsqnzcitI3KL9p5RQ5gp?usp=sharing

If you want to run locally >
Recquired environment libraries:

```
numpy
plotly
scipy
sklearn
trimesh
pandas
tqdm
pytorch
matplotlib
```

For more information please read the report
