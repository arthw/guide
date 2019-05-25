####install Conda####

https://repo.anaconda.com/archive/Anaconda3-2019.03-Windows-x86_64.exe

####install intel python####
```
conda create -n idp intelpython3_full -c intel
```

####install tensorflow with MKL (for CPU)####
```
conda install tensorflow-mkl
```
####verify tensorflow with MKL####
```
python -c "import tensorflow"
```
###download code###

https://software.intel.com/sites/landingpage/ai_courses/dc_to_the_edge.zip

conda env create  -f environment.yml

pip install opencv-python==4.1.0.25  -i https://pypi.tuna.tsinghua.edu.cn/simple



