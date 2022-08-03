cut by time

// -ss begin time;  -t end time

`ffmpeg -ss 00:00:03.0 -i input.wmv -c copy -t 00:00:13.0 output.wmv`

cut by new size

//crop=new_w:new_h:new_x:new_y

`ffmpeg -i output.mkv -filter:v "crop=1920:1030:0:0" new_size.mkv`

remove audio

`ffmpeg -i new_size.mkv -map 0 -map -0:a -c copy cut_no_audio.mkv`

