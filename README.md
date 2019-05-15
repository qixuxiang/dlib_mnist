# dlib_mnist
use dlib to run mnist 

dlib_mnist01 is for lenet and  dlib_mnist01 is for resnet, both of them can get at least 99% accuracy.

## Prerequisites
* CMake
* GCC5+
* CUDA8.0+
* dlib 19

## install dlib
```
wget -c http://dlib.net/files/dlib-19.17.tar.bz2

tar -jxvf dlib-19.17.tar.bz2

cd  dlib-19.17

mkdir build

cd build

cmake .. 

make -j4

make install

ldconfig -v

```
## Run
```
git clone https://github.com/qixuxiang/dlib_mnist

cd dlib_mnist

mkdir build && cd build

cmake ..

make -j4

mkdir mnist_data && cd mnist_data

wget -c http://yann.lecun.com/exdb/mnist/train-images-idx3-ubyte.gz

wget -c http://yann.lecun.com/exdb/mnist/train-labels-idx1-ubyte.gz

wget -c http://yann.lecun.com/exdb/mnist/t10k-images-idx3-ubyte.gz

wget -c http://yann.lecun.com/exdb/mnist/t10k-labels-idx1-ubyte.gz

gunzip *.gz 

cd .. 

./dlib_mnist01 mnist_data

./dlib_mnist02 mnist_data
```
