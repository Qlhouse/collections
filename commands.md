# Extra audio from video

ffmpeg -i sample.avi -q:a 0 -map a sample.mp3

[Reference](https://stackoverflow.com/questions/9913032/how-can-i-extract-audio-from-video-with-ffmpeg)

# Concatenate multiple audio

## Create list.txt

> file '/path/to/first.mp3'
> 
> file '/path/to/second.mp3'

## Concatenate command

`ffmpeg -f concat -i list.txt -c copy out.mp3`
