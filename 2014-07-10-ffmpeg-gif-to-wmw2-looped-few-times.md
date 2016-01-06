1. uncompressed intermediate  
`ffmpeg -i some.gif -c:v huffyuv tmp.avi`

2. looping  
`ffmpeg -i "concat:tmp.avi|tmp.avi|tmp.avi" -c copy master.avi`

3. encoding  
`ffmpeg -i master.avi -b 1500k -vcodec wmv2 -r 25 horse_loop_25.wmv`