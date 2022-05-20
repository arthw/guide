cut by time

`ffmpeg -ss 00:00:30.0 -i input.wmv -c copy -t 00:00:10.0 output.wmv`

cut by new size

`ffmpeg -i output.mkv -filter:v "crop=1920:1030:0:0" new_size.mkv`

remove audio

`ffmpeg -i new_size.mkv -map 0 -map -0:a -c copy cut_no_audio.mkv`

