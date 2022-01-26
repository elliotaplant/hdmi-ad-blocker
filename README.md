# HDMI Ad Blocker
An ad blocker for any HDMI source

# Roadmap

This project hasn't yet been started.

It will be a device that accepts an HDMI (or USB? A? C?) video stream as input and outputs an HDMI video output.

Ideally you could connect a laptop or streaming device like a chromecast to the ad blocker, and then connect the ad blocker to the TV or monitor.

A simple setup could be

Laptop --USB 3--> Ad Blocker --USB 3--HDMI-->TV

On the ad blocker, some (python?) software would periodically capture a frame from the input video stream. The software would use the frame as input to a trained machine learning model to determine whether or not the frame in question is an ad. The software would then decide to either continue passing along the unaltered input stream OR do something else (show a blank screen, show a static image (the logo of a sports bar), play from a selection of videos (like tapster from chicago), show a changing discussion question, etc. The software would continue to periodically check the input stream to see when the ads end. 

## Open questions:
- Can a raspberry pi read a video stream over USB3 from a laptop? Can it read in a video stream sent from HDMI->USB3? How would one verify that the video was playing?
- Can (python) read that video stream?
- Can (python) capture frames from that video stream?
- Can (python) send a video stream out to HDMI? Does it need to be a video file, or could it be text or a color or a picture?
- Can (python) "pass through" a video stream?
- How does one get a trained ML model onto a raspberry pi? How does one "test" an image as input to that model?

## Answering questions:
- Need a raspbbery pi 4, maybe an HDMI -> USB3 capture card
- Connect the PI to a monitor with the HDMI port
- Connect a laptop to the PI with a USBC -> USB3 cable, try to send video over the cable (will require the Pi to announce itself as a monitor, maybe?)
- Show that the video shows up on the monitor
- See if you can write some python/rust code to capture a frame of that stream
- See if you can write some python/rust to output a video stream from a file then from a color.
- Try to make that code connect the input video stream to the output
- Machine learning stuff

