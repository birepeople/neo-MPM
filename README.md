# neo-MPM
A CUDA backend MPM playground.(hopefully)

# Dependency for now
  - Eigen 
  - tinyobjloader
  - bgfx: https://bkaradzic.github.io/bgfx/
  - Nvidia CUDA toolkit >= 11.6 (for thrust and cub)

Dependencies are installed through cmake submodules ,except CUDA toolkit.
For linux Ubuntu, do:
```
sudo apt-key adv --fetch-keys http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub
sudo sh -c 'echo "deb http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64 /" > /etc/apt/sources.list.d/cuda.list'
sudo apt-get update
sudo apt-get install -y cuda-toolkit-11-6
```
As line `1`'s `ubuntu1804/x86_64/7fa2af80.pub` please refer to https://developer.download.nvidia.cn/compute/cuda/repos/ to choose your platform and backend for valid key (named `xxxxxxxx.pub`).

Line `2`'s `ubuntu1804/x86_64` should be your kernel version and platform backend.
 
Do:
```
sudo apt-get install libgl1-mesa-dev x11proto-core-dev libx11-dev
```
for bgfx build support. (Other platform should be refer https://bkaradzic.github.io/bgfx/build.html for dependency.)
