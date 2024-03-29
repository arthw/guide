```
sudo apt install build-essential
sudo apt -y install gcc-8 g++-8 gcc-9 g++-9
```

```
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-8 8
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-8 8
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-9 9
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-9 9
```

```
sudo update-alternatives --config gcc

There are 3 choices for the alternative gcc (providing /usr/bin/gcc).

  Selection    Path            Priority   Status
------------------------------------------------------------
  0            /usr/bin/gcc-9   9         auto mode
  1            /usr/bin/gcc-7   7         manual mode
* 2            /usr/bin/gcc-8   8         manual mode
  3            /usr/bin/gcc-9   9         manual mode
Press  to keep the current choice[*], or type selection number: 
```

```
sudo update-alternatives --config g++

There are 3 choices for the alternative g++ (providing /usr/bin/g++).

  Selection    Path            Priority   Status
------------------------------------------------------------
* 0            /usr/bin/g++-9   9         auto mode

  2            /usr/bin/g++-8   8         manual mode
  3            /usr/bin/g++-9   9         manual mode
```

```
gcc --version
g++ --version
```
