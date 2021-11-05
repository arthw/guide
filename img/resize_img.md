```
sudo apt-get install imagemagick
mogrify -resize 320x240 Image.png 
mogrify -resize 50% Image.png
mogrify -resize 320x240 *.jpg

### Ignore Aspect Ratio
convert demo.jpg -resize 1024x1024! demo.jpg
```
