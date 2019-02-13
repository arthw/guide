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
python3 -m pip install -U --user keras_applications==1.0.6 --no-deps
python3 -m pip install -U --user keras_preprocessing==1.0.5 --no-deps

```

#### Build with MKL
`bazel build --config=opt --config=mkl //tensorflow/tools/pip_package:build_pip_package`

#### Build PIP package
`./bazel-bin/tensorflow/tools/pip_package/build_pip_package /tmp/tensorflow_pkg`

#### Install TF by PIP
`python3 -m pip install /tmp/tensorflow_pkg/tensorflow-XXX.whl`
