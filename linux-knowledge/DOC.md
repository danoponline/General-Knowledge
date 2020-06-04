# How to connect an external monitor to an Ubuntu laptop
**Problem**: When we want to connect an external monitor to a laptop, screen will freeze. The mouse cursor can still move but we cannot click anything on the screen. This happens in both Ubuntu 16.04 and 18.04. To fix this, we need to install a VGA driver. Here is the step:
1. Figure out what VGA card model we are using. Type in terminal
 ```
 lspci | grep VGA
 ```
   Output will be something like this:
 
 ```
 01:00.0 VGA compatible controller: NVIDIA Corporation GT218M [NVS 3100M] (rev a2)
 ```
 2. Go to NVIDIA Driver Download page [here](https://www.nvidia.com/Download/index.aspx) and provide information you 
 have above.
 ![NVIDIA SCREENSHOT1](https://github.com/danoponline/cobot/blob/master/assets/nvidia_screenshot1.png?raw=true "NVIDIA SCREENSHOT1")
 
 3. We then get driver version from the next screen. Note this version number because we will use it in the next step.
 ![NVIDIA SCREENSHOT2](https://github.com/danoponline/cobot/blob/master/assets/nvidia_screenshot2.png?raw=true "NVIDIA SCREENSHOT2")
 
 4. Install the correct driver. Type in terminal
 ```
 sudo apt-get install nvidia-340
 reboot
 ```
 That's it! Now we can use an external monitor without problem.