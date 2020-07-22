# Set Up Conda Environment

## Create Conda Environment
1. Install python version 3.7.3: https://www.python.org/downloads/release/python-373/
2. Install Anaconda 3 for win10: https://www.anaconda.com/distribution/#download-section
3. Create a virtual environment and change the PYTHONPATH of an ipython kernel: 
```shell
conda update conda
conda create --name my_env python=3.7.3
conda activate my_env
conda install ipykernel -y
python -m ipykernel install --user --name my_env --display-name "my_env"
```
4. GPU support software requirements:
    * NVIDIA® GPU drivers: https://www.nvidia.com/Download/index.aspx?lang=en-us
    * CUDA® Toolkit: https://developer.nvidia.com/cuda-toolkit-archive
    * cuDNN SDK: https://developer.nvidia.com/cudnn
    * (Optional) TensorRT 5.0: https://developer.nvidia.com/tensorrt
5. Windows setup
    * Add the CUDA, CUPTI, and cuDNN installation directories to the `%PATH%` environmental variable. For example, if the CUDA Toolkit is installed to `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0` and cuDNN to `C:\tools\cuda`, update your `%PATH%` to match:
```shell
$ export PATH=C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0\bin;%PATH%
$ export PATH=C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0\extras\CUPTI\libx64;%PATH%
$ export PATH=C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0\include;%PATH%
$ export PATH=C:\tools\cuda\bin;%PATH%
```
* Add the absolute path to the TensorRTlib directory to the environment variable LD_LIBRARY_PATH
