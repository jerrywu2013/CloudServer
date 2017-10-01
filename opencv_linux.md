#### Install OpenCV 3 in Ubuntu14.04
```
sudo pip3 install numpy
sudo pip3 install --upgrade pip
sudo pip3 install jupyter
```
```
$ sudo apt-get update 
$ sudo apt-get upgrade 
$ sudo apt-get install build-essential cmake git pkg-config 
$ sudo apt-get install libjpeg8-dev libtiff4-dev libjasper-dev libpng12-dev 
$ sudo apt-get install libgtk2.0-dev 
$ sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev 
$ sudo apt-get install libatlas-base-dev gfortran 
$ cd ~ 
$ git clone   https://github.com/Itseez/opencv.git 
$ cd opencv 
$ git checkout 3.1.0 
$ cd ~/opencv 
$ mkdir build 
$ cd build 
$ cmake -D CMAKE_BUILD_TYPE=RELEASE \ 
        -D   CMAKE_INSTALL_PREFIX=/usr/local \ 
        -D   INSTALL_C_EXAMPLES=OFF \ 
        -D   INSTALL_PYTHON_EXAMPLES=ON \ 
        -D   OPENCV_EXTRA_MODULES_PATH=~/opencv_contrib/modules \
        -D   BUILD_EXAMPLES=ON ..
   
$ make -j4
$ sudo make install
$ sudo ldconfig
```
