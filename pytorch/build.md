# Build Pytorch for Intel GPU from Source
```
conda create -y -n build_torch
conda activate build_torch
git clone https://github.com/NeoZhangJianyu/pytorch
cd pytorch
git submodule sync
git submodule update --init --recursive
conda install cmake ninja
pip install -r requirements.txt
pip install mkl-static mkl-include
.ci/docker/common/install_magma_conda.sh 12.4


export USE_XPU=1
make triton
export CMAKE_PREFIX_PATH=/home/jianyuzh/miniforge3/envs/build_torch
source /opt/intel/oneapi/setvars.sh 
python -m pip install --no-build-isolation -v -e .

```
