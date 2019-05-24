### Cut video ###
```
ffmpeg -i example.avi -vf crop=a:b:c:d  outputfilename
```
```
a: width
b: height
c: left
d: top
unit: pixel
```
