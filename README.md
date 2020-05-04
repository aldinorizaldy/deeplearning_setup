# Deep Learning Setup on Ubuntu

Assume we don't have Ubuntu. Only Windows (as we always do). Then we want to setup Deep Learning Framework (e.g. Tensorflow) on Ubuntu.
Things we should do:

The Only Hardware Requirement: nvidia GPU (we can do this without GPU, but where is the fun?)

A. Install Ubuntu dual-mode with Windows
We have Windows and we want to have Ubuntu as well for the deep learning (almost all deep learning codes in github are written in Ubuntu, we always could modify the codes but for the sake of simplicity we don't want to modify the given codes that much). 
1. Download Ubuntu installer ISO image from website. Choose between 18.04 or 16.04.
2. Download 3rd party software rufus to create bootable USB flash drive.
3. Change the boot directory in BIOS. To enter BIOS mode, it depends on the machine but usually done by pressing F2 or DEL button when the machine boots. Reboot.
4. Install Ubuntu. Click Next until finish.
5. Now, we have options every time the machine boots. Ubuntu on the first option (and will be chosen if we don't do anything) and Windows on the third option. It's a nice idea to have dual OS so we don't lose all things we love in Windows.

B. Install nvidia CUDA
1. Check nvidia driver. nvidia-smi
2. Make sure there is no previos CUDA installation.
3. Download CUDA installer from nvidia website. Choose which version we want to use. Remember the compatibility issue with the deep learning framework. For instance, Tensorflow 2.1.0 requires CUDA 10.2. Older version of Tensorflow requires older version of CUDA as well. Also please remember what codes we want to work with. Some codes were built under older version of Tensorflow, and there is no guarantee the codes would running well in the newer version of Tensorflow. One thing for sure, codes in Tensorflow 1 will not run on Tensorflow 2, and the other way around. We need to migrate the codes. Up to now, I see most of codes in github were built in Tensorflow 1.   
4. 

C. Install cuDNN libraries
D. Install Tensorflow-GPU


alternate install
CTRL + ALT + F1 # masuk ke tty1
sudo service lightdm stop # stop GUI
init 3 # kalo bisa, tapi bisa jadi nggak bisa
cd /path/to/the/run/file/
sudo sh cuda_xx.x.xxx_xxx.xx_linux.run
sudo service lightdm start # kembalikan GUI (opsional) bisa langsung reboot
