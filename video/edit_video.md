## cut by time

// -ss begin time;  -to time long

`ffmpeg -ss 00:00:03.0 -i input.wmv -to 00:00:13.0 output.wmv`

## cut by new size

//crop=new_w:new_h:new_x:new_y

`ffmpeg -i output.mkv -filter:v "crop=1920:1030:0:0" new_size.mkv`

## video to audio

`ffmpeg -i filename.mp4 filename.mp3`

## remove audio

`ffmpeg -i new_size.mkv -map 0 -map -0:a -c copy cut_no_audio.mkv`

## convert image to video

`ffmpeg -r 30 -f image2 -s 1920x1080 -i cartoon_%04d.png -vcodec libx264 -crf 25  -pix_fmt yuv420p test.mp4`

## merge videos to one

```
list.txt: 
file ollama_0.mp4
file ollama_1.mp4

ffmpeg -f concat -i  list.txt -codec copy ollama.mp4
```


 
