# Tensorflow_on_Raspberrypi
TensorFlow is an open-source machine learning library developed by Google that is widely used in the field of artificial intelligence. It can be installed on various platforms including Raspberry Pi, which is a popular single-board computer used in various projects. Here's a step-by-step guide on how to install TensorFlow on Raspberry Pi:

1. Install an operating system(recommended aarch64 OS -> Ubuntu Server 22.04.2 LTS (64-bit)) on A Raspberry Pi (Model 3 or later).

2. Update and Upgrade the Raspberry Pi:
  The first step is to update and upgrade the Raspberry Pi to ensure that we have the latest packages and software.
  ```bash
  sudo apt update
  sudo apt upgrade -y
  ```
3. Install the Dependencies:
The next step is to install the dependencies required by TensorFlow.
```bash
sudo apt-get install -y libhdf5-dev libc-ares-dev libeigen3-dev gcc gfortran libgfortran5 libatlas3-base libatlas-base-dev libopenblas-dev libopenblas-base libblas-dev liblapack-dev cython3 libatlas-base-dev openmpi-bin libopenmpi-dev python3-dev pip install -U wheel mock six
```
4. Find your .whl file
   - Check Architecture : 
       ```bash
       uname -m
       ```
       this prints the architecture of the system ```aarch64``` or ```armv7l```(recommended to use ```aarch64``` OS because the latest version of tensorflow wheels only support ```aarch64```)
   
   - Check Python Version:
   ```bash
   python3 -V
   ```
   this will display the python version ```Python 3.*.*```
   
   - Open this link [Tensorflow Wheels](https://github.com/PINTO0309/Tensorflow-bin/tree/main/previous_versions) to choose the wheel for your PI
   the format to which u need to choose
   ```bash
   download_tensorflow-2.*.*-cp<python-version>-none-linux_<architecture>.sh
   ```
   - choose the bash file according to your python version(```cp-39``` means python-3.9.*) and architecture(```aarch64``` or ```armv7l```)
   in this experiment we used : 
   ```bash
   download_tensorflow-2.9.0-cp39-none-linux_aarch64.sh
   ```
   - __Select "view raw" then copy the URL__
   
   __Note__ :if your python version is not there then you need to change your python version you can reffer this [link](https://github.com/pyenv/pyenv) to change python versions
    
    - download the wheel file 
    ```bash
    wget [RAW file url]
    ```
    
    - then change that file permission to executable file
    ```bash
    chmod +x download_tensorflow-2.9.0-cp39-none-linux_aarch64.sh
    ```
    
    - Run that file to download the wheel file for tensorflow
    ```bash
    ./download_tensorflow-2.9.0-cp39-none-linux_aarch64.sh
    ```
    
    - 
    
   
   
