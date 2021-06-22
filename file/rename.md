### Rename all *.JPEG files in subfolders to jpg
```
find .  -name "*.JPEG"   -exec sh -c 'f="{}"; echo "$f" "${f%.JPEG}.jpg"' \;
```
