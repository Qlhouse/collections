# Extra audio from video

ffmpeg -i sample.avi -q:a 0 -map a sample.mp3

[Reference](https://stackoverflow.com/questions/9913032/how-can-i-extract-audio-from-video-with-ffmpeg)

# ffmpeg split video

ffmpeg -ss 01:31:50 -t 04:29:39 -i 'Creating an Online Chat App.mp4' -acodec copy -vcodec copy 'Creating an Online Chat App Part B.mp4'

-ss, 开始时间

-t, 结束时间

-i, 输入的文件名

# Concatenate multiple audio

## Create list.txt

> file 'C:\Users\xq127\Downloads\Video\11.mp3'
>
> file 'C:\Users\xq127\Downloads\Video\22.mp3'
>
> file 'C:\Users\xq127\Downloads\Video\33.mp3'

## Concatenate command

`ffmpeg -f concat -i list.txt -c copy out.mp3`

ffmpeg视频合并Unsafe file name问题解决: 加个`-safe 0` 参数

ffmpeg.exe -f concat -safe 0 -i ./fileToMerge.txt -c copy -y ./out.mp4

# npm 换源

npm config set registry https://registry.npm.taobao.org

# Powershell jump into WSL

wsl -d debian

