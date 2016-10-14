## Installing Tensorflow on Ubuntu 14.04
```
wget https://repo.continuum.io/archive/Anaconda3-4.2.0-Linux-x86_64.sh
bash Anaconda3-4.2.0-Linux-x86_64.sh
sudo apt install -y python-dev python-pip python-nose gcc g++ git gfortran vim
sudo apt install -y libopenblas-dev liblapack-dev libatlas-base-dev
sudo pip3 install keras
sudo pip install keras

sudo pip install ipython notebook
ipython notebook
import keras
```
```
cd /anaconda3/bin
anaconda search -t conda keras
./conda install -c KEHANG keras=1.0.8
./conda install tensorflow
./jupyter-notebook
```
```
from keras.models import Sequential
Using TensorFlow backend.
```
http://127.0.0.1:8976/

