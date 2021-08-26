
TROUBLESHOOTING
===============

**Get help online:** https://github.com/magdesign/PocketVJ-CP-v3/issues

There will always be a solution :-)

Not able to connect CP via browser
***********************************

.. note::
    Some browsers force a https:// connection, which is not possible on PocketVJ and will cause trouble to not be able to connect.

If you try to connect the CP via webbrowser and get an error like this:


.. image:: _images/15_unable_to_connect.png


then all you have to do is to remove the  https:// in the addressbar:


.. image:: _images/15_disable_https.png

**After update CP is showing a blank page**

=> Do again an update, but with the alternative method:
https://video.pocketvj.com/AVideo/video/41/pocketvj-rtc-alternative-update

**Movie plays, but stutters** 
******************************
=> Check if it is really a h.264 compressed movie.

**I dont get an IP address from the PocketVJ** 
**********************************************
=> Be patient, try again. Check the preferences on your device.

.. note::
    Sometimes there are power peaks which can cause that the Wifi signal is not strong enough.
    Known are some issues with Hdmi to VGA adapters with old VGA devices who suck a lot of power.
    Also after plugging in some USB sticks. If there are many wireless devices in the room, change the wifi channel, since most units use channel 6 as standard.


**Can't connect via WIFI or constantly loosing WIFI connection**
*****************************************************************
=> Not enough power from the powersupply, connect via RJ45 and check if you get enough power in SYSTEM SETTINGS.
You need 5V and 3A, lower Amps will not work!

=> Try connecting via direct RJ45 https://video.pocketvj.com/AVideo/video/20/direct-rj45-to-your-pocketvj

**Movie is not playing**
************************
- Make sure that there is no space or special character in the filename and it is not longer than 16 characters, my_video_file.mp4 not: my video file.mp4.
- Make sure your video is converted with the h264 codec (this causes in most cases the error)
- Make sure your video data is in the correct folder (/media/internal/video/).
- Make sure your PocketVJ is not configured to ‘Slideshow’ mode.
- Make sure audio output is set to HDMI/ Jack or both if there is no external soundcard connected, otherwise it will search for the ALSA device and will not start.

**USB-Stick does not work anymore on my computer** 
**************************************************
=> Plug it back into the PocketVJ and Click UNMOUNT in the control panel.

Make sure to always mount and unmount your USB devices!

**Connected several PocketVJs over a router**
*********************************************
- Check the Gateway settings of your router, in original mode the PocketVJ runs in 192.168.2.1

**Remote “Power On Projector” does not work**
*********************************************
- Login to projector, enable PJLink, disable all passwords
- Under Service, enable DDDP and set the Crestron control IP to: 192.168.2.254
- make sure the Projector has following network info:


``IP: 192.168.2.254``

``Subnet: 255.255.255.0``

``Default Gateway: 192.168.2.1``

``DNS Server: 192.168.2.1``

- check this troubleshoot video: https://video.pocketvj.com/AVideo/video/25/pocketvj-pjlink-a-projector
- make sure the computer which is connected to the PocketVJ CP is not connected to second network, for example RJ45 in your local network and wifi to PocketVJ, 
if this is the case, unplug rj45 until it finds the projector, then you can plug it in again. Get a list of standard passwords for projectors here: https://github.com/magdesign/PocketVJ-CP-v3/blob/master/projector_passwords.md



CREATE h264 MOVIES
******************

Best way to do this is using https://handbrake.fr

Beleive me, the Adobe codecs are crap!





**Finally, after several hours I reached the end of the documentation, if there is somethingn wrong or missing, please tell me!**