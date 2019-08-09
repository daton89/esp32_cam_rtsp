# esp32_cam_rtsp #

This example works for esp32 ai thinker dev kit.

The project is built with platform.io and vscode.

## Getting started ##

`git clone https://github.com/daton89/esp32_cam_rtsp.git`

Rename the file with wifi credentials running `cp include/wifikeys_example.h include/wifikeys.h` and replace the informations with your data.

Now flash the device:

`pio run -t upload # (This command will fetch dependencies, build the project and install it on the board via USB)`

To check that everything is working and to get the ip address of the device open the serial monitor:

`pio serial monitor`

To see the camera from the browser:

`open http://192.168.0.19 # replace with camera ip from serial monitor`

To see the RTSP stream using VLC:

`vlc -v rtsp://192.168.0.19:8554/mjpeg/1`