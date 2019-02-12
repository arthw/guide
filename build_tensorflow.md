### In Ubuntu 16 for Python3
#### Set proxy for bazel
```
export HTTP_PROXY=http://xxx.com:913
export HTTPS_PROXY=http://xxx.com:913
```
#### Install python package
```
sudo apt install python3-dev python3-pip
python3 -m pip install six numpy wheel mock
```

#### Build with MKL
`bazel build --config=opt --config=mkl //tensorflow/tools/pip_package:build_pip_package`
