### Rename all *.JPEG files in subfolders to jpg
```
find .  -name "*.JPEG"   -exec sh -c 'f="{}"; mv "$f" "${f%.JPEG}.jpg"' \;
```
