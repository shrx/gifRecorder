gifRecorder
==========
gifRecorder is a simple bash script to record the activity on your OS X screen and save it as a GIF animation. I made it because there was no similar tool for OS X like there is [byzanz][1] for Linux.
This is done using the gif processing tool, Gifsicle.

[1]: http://linuxers.org/article/byzanz-record-record-your-desktop-session-gif-image

Prerequisites, dependencies
---------------------------
You need to have [Gifsicle][2] installed for this script to work.

[2]: http://www.lcdf.org/gifsicle/man.html

Usage
-----
Run the script when you want to record your screen activity.

The script first create a temporary directory for screenshots, then combine the screenshots into a GIF animation and export it to your desktop.

The default recording duration is 5 seconds. You can change this by running the script with the option `-s <seconds>`, for example: `gifRecorder -s 10` will record for 10 seconds.

By default the script will record your entire screen. You can also specify the dimensions of the rectangle you want to be recorded with the option `-c x1,y1-x2,y2`. The top-left corner of this rectangle is at `(x1,y1)` and the lower-right corner is at `(x2,y2)`. For example: `-c 0,0-1439,21` will capture just your menu bar.

You can also enable the verbose mode with the option `-v`.