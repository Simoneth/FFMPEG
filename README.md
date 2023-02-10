# FFMPEG

ffmpeg -i input -vf "scale=100:-1,setdar=16/9" output

ffmpeg -i input_file -ss start -to end -filter:v "scale=iw*min({}/iw\\,{}/ih):ih*min({}/iw\\,{}/ih),crop={}:{}'.format(width, height, width, height, width, height)" -c:v=libx264 -crf=18 -an -c:a=anull output_file
  
  
https://bnb2022193349-dev.s3.eu-central-1.amazonaws.com/public/uploads/org/canvas/static/1080p.mp4
