# dominant_color_case_study
**In this case study we find out  the Most Dominant Color in an image. Image is given below.**
![alt text](https://i.imgur.com/eG9iRHd.jpg)

# You're given this t-shirt.
**We can clearly see that the most dominant colour here is black.
But how will a program know the colour of the t-shirt?**

To handle visual objects v.i.z. Image and Videos, python provides us with **an amazing module cv2.**
cv2 implements all the functionalities of the Computer Vision field of science. 
Computer vision tasks are nothing but methods for acquiring, processing, analyzing and understanding digital images.

It's really easy to read an image into your python script.
The cv2 module provides us with a function called imread() which accepts the image name and loads it into a numpy array.

We mentioned something about a numpy array.
NumPy is the fundamental package for scientific computing with Python.
It helps us to define multidimensional arrays (more than 2 dimensions) which is otherwise impossible to handle.


# Python setup:
To properly use this python-modules some additional libraries have to be installed beforehand. This can be easily accomplished with the commands below.
- pip install opencv-python
- import cv2

# we're going to learn about another Machine Learning algorithm known as K Means clustering.
Let's try to understand the intuition behind the algorithm
![alt text](https://i.imgur.com/Hejigdo.png) 

**Consider the given plot of data**

Can you identify two different classes in this data set?

What will you do if you're ask to label the plot into two classes?

You will try to find similar data points and then group them together. Right?

**K Means clustering makes it even easier.**

# STEP 1

Choose a value of K. This has to be equal to the number of classes you want in your output.

The value of K is decided intuitively.

It is only with practise that you learn to decide the best possible value of K by just looking at the plot of data.

For our example, let K be equal to 2.

# STEP 2

Once the value of K has been decided, the algorithm proceeds to choose K random points on the plot.

These points don't have to belong to our data set.

**Let's choose two random points as follows.**
![alt text](https://i.imgur.com/BYbsDo8.png) 

These points are called **initial centroids.**

**Why are they called centroids?**

This is because they are assumed to be the centres of the clusters that we are going to form.

We will see why is it an assumption.

# STEP 3

Assign each data point to the closest centroid.

To do this, distance of each point is calculated from the two centroids.

The data point is assigned to the centroid whichever is closest to it.
Another method to do this is to draw a line such that every point on it is equidistant from both the centroids.
![alt text](https://i.imgur.com/veKo7XW.png) 

**The line represented by green is such a line.**

Now every point on the left side of this line is closer to the blue centroid.

And likewise, every point to the right of this line is closer to the red centroid.

Another method to do this is to draw a line such that every point on it is equidistant from both the centroids.



The line represented by green is such a line.
Now every point on the left side of this line is closer to the blue centroid.

And likewise, every point to the right of this line is closer to the red centroid.

Therefore, we can form the two clusters as follows: 
![alt text](https://i.imgur.com/4FOKZ9d.png) 

# STEP 4

Find new centroids of the obtained clusters.

Since the centroids were chosen at random, they are different from the centroid of the clusters obtained.

Hence we find and assign new centroids for each of the clusters.

![alt text](https://i.imgur.com/asK8vnO.png) 

# STEP 5

Reassign each data point to the new closest centroid. If any reassignment took place, go to step 4, otherwise stop and save the clusters.

Since new centroids were obtained in last step, we need to reassign the data points to each cluster.

We do this again by drawing the line equidistant from both the centroids.
![alt text](https://i.imgur.com/HqY1YTq.png) 

We can see that a couple of points needs to be assigned new clusters.

Let's reassign the clusters to these points: 
![alt text](https://i.imgur.com/HqY1YTq.png)

We now go back to step 4 since there was reassignment of points.

The new centroids are as follows: 
![alt text](https://i.imgur.com/EMiV49U.png)

Let's see if there is a reassignment needed. 
c

One of the data points needs to be assigned a new cluster.

We do that and proceed to step 4 once again.

This is how our plot looks like after reassignment.

![alt text](https://i.imgur.com/8Gnqp6P.png)

Let's find new centroids once again. 
![alt text](https://i.imgur.com/LQuKJUb.png)

We repeat the process of reassignment. 
![alt text](https://i.imgur.com/jCDwo9N.png)

Reassigning clusters to the data points.
![alt text](https://i.imgur.com/Ez91RLQ.png)

Once again, we proceed to find new centroid for our clusters. 
![alt text](https://i.imgur.com/I8y8JqG.png)

This time we find that there is no reassignment required.
![alt text](https://i.imgur.com/TIfGPYk.png)

Hence the algorithm concludes its iterations and assigns the classes blue and red to the data points according to their clusters.

We were able to classify the data into separate classes without knowing anything about their classes beforehand.

**This is exactly how K Means algorithm works.**
