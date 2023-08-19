# Installing gstreamer 

 https://gstreamer.freedesktop.org/download/ 
 ref: https://gstreamer.freedesktop.org/documentation/installing/on-windows.html?gi-language=c

 after install and put plugin to path 
 set  "C:\gstreamer\1.0\mingw_x86_64\bin" plugin to windows path by 

 searching Edit environment variables,  and follow:
 / System Properties/ Environment Variables/used variables for "Username"/ Path -  create new path - "C:\gstreamer\1.0\mingw_x86_64\bin". 

gst-inspect-1.0
200 plugins, 1532 features are found

 Installing actaul gstreamer plugin to see gstreamer inside obs studio
 OBS studion gstreamer      https://obsproject.com/download
 tutorial:   https://www.youtube.com/watch?v=qZWFuTCKNeQ
 install obs-gstreamer.zip:     https://github.com/fzwoch/obs-gstreamer/releases/tag/v0.3.0

 copy obs-gstreamer.dll file and paste inside "C:\Program Files\obs-studio\obs-plugins\64bit", and now gstreamer source will show up in obs studion app.



 for Gstreamer projects around 29 all link below:
 https://www.youtube.com/playlist?list=PLfFan4sDonOccKApSxnb8mZyUS3CLxSMF 

# filesrc .mp4 example 
    gst-launch-1.0 filesrc location=D:/projects/gstreamer/HyundaiCon_videos/YUN_0006.MP4 ! qtdemux ! h264parse ! avdec_h264 ! autovideosink
 the pipeline qtdemux ! h264parse ! avdec_h264 ! autovideosink reads the video file in MP4 format, extracts the H.264 video stream, decodes it using the H.264 decoder, and displays the video frames on the screen using an appropriate video sink. The pipeline assumes that the video file is in H.264 format inside an MP4 container, and it processes it for rendering on your screen

 qtdemux: This element is responsible for demuxing (extracting) multimedia data from the MP4 container format (also known as QuickTime or MOV format). The MP4 format can contain multiple streams, such as video, audio, and subtitles, and qtdemux separates these streams and sends them to their respective downstream elements for further processing.
# h264parse: In the context of this pipeline, h264parse is used to parse the H.264 video stream extracted by qtdemux. The H.264 codec is a widely used video compression standard, and h264parse is used to handle the H.264-specific properties and data format. It ensures that the downstream element, 

 avdec_h264: This element is responsible for decoding the H.264 video stream into raw video frames. It takes the compressed H.264 bitstream and decodes it into an uncompressed format that can be displayed or further processed. The decoded frames are then sent to the next element, autovideosink.
 
 autovideosink: The autovideosink element is an element that automatically selects and uses an appropriate video sink based on the available environment and platform. In your case, it is likely using a default video sink suitable for your system, such as Direct3D on Windows or X11 on Linux. The video sink is responsible for displaying the decoded video frames on the screen.


# filesrc webcam 
# ref tutorial: https://www.youtube.com/watch?v=RA_coHkCdwg&list=PLfFan4sDonOccKApSxnb8mZyUS3CLxSMF&index=2




