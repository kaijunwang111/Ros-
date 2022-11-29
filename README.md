# ros-noetic installation (for ubuntu 20.04)

<http://wiki.ros.org/noetic/Installation/Ubuntu>
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'  
sudo apt install curl # if you haven't already installed curl  
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -  
sudo apt update  
sudo apt install ros-noetic-desktop-full  
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc  
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential  
sudo apt install python3-rosdep  
sudo rosdep init  
rosdep update  
```
If there is a problem "E: Unable to correct problems, you have held broken packages.", use "aptitude", and search for different solutions by tapping "n".
```
sudo apt install aptitude  
sudo aptitude install ros-noetic-desktop-full  
```

# ceres-solver

```
git clone https://github.com/ceres-solver/ceres-solver
```

## install dependencies
```
# CMake  
sudo apt-get install cmake
# google-glog + gflags  
sudo apt-get install libgoogle-glog-dev libgflags-dev
# Use ATLAS for BLAS & LAPACK  
sudo apt-get install libatlas-base-dev
# Eigen3  
sudo apt-get install libeigen3-dev
# SuiteSparse (optional)  
sudo apt-get install libsuitesparse-dev
```
## build & install
```
mkdir build && cd build  
cmake ..  
make -j8  
sudo make install  
```

# opencv

<https://opencv.org/releases/>  
Choose a version and download sources.

## install dependencies
```
sudo apt-get install build-essential libgtk2.0-dev libavcodec-dev libavformat-dev libjpeg-dev libswscale-dev libtiff5-dev  
sudo apt-get install libgtk2.0-dev  
sudo apt-get install pkg-config  
```
## build & install
```
mkdir build && cd build  
cmake ..  
make -j8  
sudo make install  
```

# pcl

```
sudo apt install libpcl-dev
```

# Eigen3

<https://eigen.tuxfamily.org/>  
Choose a version and download it.  

```
mkdir build && cd build  
cmake ..  
make -j8  
sudo make install  
```

# Sophus

## install fmt
```
git clone https://github.com/fmtlib/fmt.git
cd fmt
mkdir build && cd build  
cmake ..  
make -j8  
sudo make install  
```

## install Sophus
```
git clone https://github.com/strasdat/Sophus.git
cd Sophus
mkdir build && cd build  
cmake ..  
make -j8  
sudo make install  
