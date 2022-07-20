#### **cautious-journey** 

# **Lidar Car Detection**

### **Introduction**

Self-driving cars have a number of cameras at every angle to collect maximum data about their surrounding. Along with traditional cameras, they also have advanced radar systems.

**What is LiDAR?**

LiDAR is an advanced radar system used by self-driving cars. It is one of the most important technologies that produce a 3D digital representation of cars surrounding environment. This device sends out pulses of light that bounce off an object and returns back to the LiDAR sensor which determines its distance. 

Given 3D LiDar data points, our goal is to predict how many cars are around our self-driving vehicle.

The challenge is to use the 3D car lidar features from the dataset to build an automated algorithm to predict how many vehicles were there in the lidar range; in machine learning terms: this is a regression task.

### **Dataset**

The dataset represents the 3D lidar points generated using Carla Simulator. It contains two columns in which the - 
- the first column contains the x, y, and z points of the 3D Lidar Data
- the second column contains the label ( number of vehicles )

### **Files**

Following files are to be downloaded:

- train.npz ( 399 samples ) - The training dataset contains the 3D lidar points in the first column and labels in the second column. To read the file in python, you can use NumPy.

- test.npz ( 601 samples ) - Unlike the training file, it contains only the 3D lidar points and not the labels.

### **Downloading Dataset**

First you need to install ```aircrowd-cli``` by running the following command on jupyter notebook.
```python
!pip install aicrowd-cli
%load_ext aicrowd.magic
```

```
%aicrowd login
```

And then save the dataset in a folder ```/data/```.
```python
!rm -rf data
!mkdir data
%aicrowd ds dl -c lidar-car-detection -o data
```
