# How To Create Animated GIF In Linux

### Make GIF images from a Video

- we need to install FFmpeg, and ImageMagick to create GIFs    
        ```
        $ sudo apt-get install ffmpeg imagemagick
        ```
- convert two video files into GIF format using FFmpeg
        ```
        $ ffmpeg -ss 00:00:20 -i sample.mp4 -to 10 -r 10 -vf scale=200:-1 cutekid_cry.gif
        ```
        here:
          - **-ss** : indicates the starting point of GIF
          - **-i** : input file
          - **sample.mp4** : My video file name
          - **-to** : End position of the GIF file
          - **-r** : frame rate. You can increase the value to get more quality GIF file
          - **-vf** : filter graph. To scale the GIF image in the desired size.

### Combine multiple GIFs into one

```
$ convert -delay 120 -loop 0 \*.gif cutekids_crying.gif
```

### Create GIF from a list of images
```
$ convert -delay 120 -loop 0 *.jpg linux.gif
```
here:
   - -delay 120 : The GIF animation speed
   - -loop 0 : Infinite loops of the animation.
