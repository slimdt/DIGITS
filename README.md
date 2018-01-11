# DIGITS
install DIGITS on Ubuntu16.04 <br />
sliM & D.T. <br />
2018-01-09 <br />
Notice that: Most of the references are written in Chinese.

## Step 1 Install UBUNTU16.04
Ref: [link](http://www.cnblogs.com/Duane/p/6776302.html"Chinese").
## Step 2 Install CUDA AND cuDNN
### Step 2.1 Install NVIDIA driver
Ref: [link](http://blog.csdn.net/cdwxx1234/article/details/75121562 "Chinese").
Problem: nvidia-smi command not found <br/>
Solution: disable secure boot, you may set up a supervisor password before trying to disable secure boot <br/>
### Step 2.2 Install CUDA8.0
Ref: [link](http://blog.csdn.net/cdwxx1234/article/details/75121562 "Chinese").<br/>
Ref: [link](http://blog.csdn.net/autocyz/article/details/52299889/ "Chinese").
### Step 2.3 Install cuDNN V5.1
download cudnn <br/>
Ref: [link](https://developer.nvidia.com/rdp/cudnn-archive "Chinese").<br/>
install cudnn
Ref: [link](http://blog.csdn.net/cdwxx1234/article/details/75121562 "Chinese").<br/>
Ref: [link](http://blog.csdn.net/jhszh418762259/article/details/52958287?locationNum=8&fps=1 "Chinese").<br/>

error: /sbin/ldconfig.real: /usr/local/cuda-8.0/targets/x86_64-linux/lib/libcudnn.so.5 is not a symbolic link <br/>
solution: sudo ln -sf /usr/local/cuda-8.0/targets/x86_64-linux/lib/libcudnn.so.5.0.5 /usr/local/cuda-8.0/targets/x86_64-linux/lib/libcudnn.so.5 <br/>
## Step 3 Install caffe and digits
Ref: [link](http://blog.csdn.net/cdwxx1234/article/details/76043638 "Chinese").<br/>

### Step 3.1 Install dependences
### Step 3.2 Install pip and easy-install
### Step 3.3 Install caffe and python dependences
#### Step 3.3.1 Install pip
#### Step 3.3.2 Clone caffe
#### Step 3.3.3 Install dependences in /caffe/python/
error: 
solution: create a .sh file which contains<br/>
for req in $(cat "requirements.txt"); do pip install $req; done <br/>
then run sudo -H ./a.sh
### Setp 3.4 Compile Caffe
error:<br/>
/usr/bin/ld: cannot find -lhdf5_hl<br/>

/usr/bin/ld: cannot find -lhdf5<br/>

/usr/bin/ld: cannot find -lopenblas<br/>

collect2: error: ld returned 1 exit status<br/>

Makefile:567: recipe for target'.build_release/lib/libcaffe.so.1.0.0-rc3' failed<br/>

make: *** [.build_release/lib/libcaffe.so.1.0.0-rc3] Error 1<br/>
solution: Ref: [link](http://blog.csdn.net/cdwxx1234/article/details/75136657 "Chinese").<br/>
Hint: find -name "libhdf5_serial.so.10.1.0"

error: pytest error, no pydot<br/>
solution: <br/>
sudo -H pip install pydot<br/>
sudo -H pip install pydot graphviz<br/>
this solution triggered a new error: no dot found in the path <br/>
solution: sudo -H apt install python-pydot python-pydot-ng graphviz <br/>
You may skip the previous solution and use this solution directly, anyway I did not try.
### Step 3.5 Install DIGITS
Ref: [link](https://github.com/NVIDIA/DIGITS/blob/master/docs/Configuration.md).<br/>









