# FFMPEG

ffmpeg -i input -vf "scale=100:-1,setdar=16/9" output

start = '00:00:00'  # start time in HH:MM:SS format
end = '00:00:05'  # end time in HH:MM:SS format

ffmpeg -i https://bnb2022193349-dev.s3.eu-central-1.amazonaws.com/public/uploads/org/canvas/static/1080p.mp4 -ss "00:00:00" -to "00:00:05" -filter:v "scale=iw*min({}/iw\\,{}/ih):ih*min({}/iw\\,{}/ih),crop={}:{}'.format(405, 720, 405, 720, 405, 720)" -c:v=libx264 -crf=18 -an -c:a=anull output_file.mp4
  
  
https://bnb2022193349-dev.s3.eu-central-1.amazonaws.com/public/uploads/org/canvas/static/1080p.mp4
