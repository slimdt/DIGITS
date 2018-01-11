# DIGITS
install DIGITS on Ubuntu16.04 <br />
sliM & D.T. <br />
2018-01-09 <br />

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






