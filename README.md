# cast-play-test
check advertised audio format support for google cast devices

# why

recent google cast audio devices run a new firmware version (google cast for audio 2.0, also known as castlite) ... these devices can incorrectly advertise which audio formats they support, which can cause unnecessary transcodes or playback failure for apps that check format support before starting playback ... see instructions below for how to test your cast device ... share test results with your device manufacturer and request firmware fixes if there are issues!

# how to

1) go to google's command and control tool website [Cactool V2](https://casttool.appspot.com/cactool/)<br>
2) set the receiver App ID to `D7D5D949`<br>
3) click the cast icon at the top of the browser page, select your cast device from the list<br>
4) the cast icon should indicate that the app is loaded<br>
5) scroll down, logged test results should show at the bottom of the page<br>

# test results

example results from 3 devices below (Wiim Ultra, Wiim Pro Plus, and Google Chromecast Audio)
Wiim Ultra runs the newer castlite firmware, the others run the older/original chromecast firmware
each test run shows UserAgent for the tested device, then the canDisplayType and canPlayType results for a number of common audio formats 
```
[ 2.736s] [PlayTest] [INFO] END
[ 2.735s] [PlayTest] [INFO] UserAgent: Castlite/1.0 (Linkplay Technology Inc.; WiiM Ultra) CrKey/1.68.000001
[ 2.735s] [PlayTest] [INFO] format,canDisplayType,canPlayType
[ 2.734s] [PlayTest] [INFO] audio/wav,false,false
[ 2.732s] [PlayTest] [INFO] audio/ogg; codecs=vorbis,false,false
[ 2.731s] [PlayTest] [INFO] audio/ogg; codecs=opus,false,false
[ 2.730s] [PlayTest] [INFO] audio/mpeg,true,probably
[ 2.728s] [PlayTest] [INFO] audio/mp4; codecs=mp4a.40.2,true,probably
[ 2.717s] [PlayTest] [INFO] audio/mp4; codecs=alac,false,false
[ 2.715s] [PlayTest] [INFO] audio/mp3,true,probably
[ 2.714s] [PlayTest] [INFO] video/matroska; codecs=opus,false,false
[ 2.712s] [PlayTest] [INFO] audio/flac,false,false
[ 2.710s] [PlayTest] [INFO] audio/ape,false,false
[ 2.708s] [PlayTest] [INFO] audio/aiff,false,false
[ 2.706s] [PlayTest] [INFO] audio/aac,true,probably
[ 2.699s] [PlayTest] [INFO] START
[ 2.697s] [PlayTest] [INFO]
[ 2.532s] [PlayTest] [INFO] END
[ 2.530s] [PlayTest] [INFO] UserAgent: Mozilla/5.0 (X11; Linux aarch64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.225 Safari/537.36 CrKey/1.56.500000
[ 2.529s] [PlayTest] [INFO] format,canDisplayType,canPlayType
[ 2.527s] [PlayTest] [INFO] audio/wav,true,maybe
[ 2.524s] [PlayTest] [INFO] audio/ogg; codecs=vorbis,false,probably
[ 2.522s] [PlayTest] [INFO] audio/ogg; codecs=opus,false,probably
[ 2.519s] [PlayTest] [INFO] audio/mpeg,true,probably
[ 2.516s] [PlayTest] [INFO] audio/mp4; codecs=mp4a.40.2,true,probably
[ 2.507s] [PlayTest] [INFO] audio/mp4; codecs=alac,false,false
[ 2.504s] [PlayTest] [INFO] audio/mp3,true,probably
[ 2.501s] [PlayTest] [INFO] video/matroska; codecs=opus,false,false
[ 2.498s] [PlayTest] [INFO] audio/flac,true,probably
[ 2.495s] [PlayTest] [INFO] audio/ape,false,false
[ 2.491s] [PlayTest] [INFO] audio/aiff,false,false
[ 2.488s] [PlayTest] [INFO] audio/aac,true,probably
[ 2.482s] [PlayTest] [INFO] START
[ 2.479s] [PlayTest] [INFO]
[ 2.623s] [PlayTest] [INFO] END
[ 2.622s] [PlayTest] [INFO] UserAgent: Mozilla/5.0 (X11; Linux armv7l) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.225 Safari/537.36 CrKey/1.56.500000
[ 2.620s] [PlayTest] [INFO] format,canDisplayType,canPlayType
[ 2.618s] [PlayTest] [INFO] audio/wav,true,maybe
[ 2.615s] [PlayTest] [INFO] audio/ogg; codecs=vorbis,false,probably
[ 2.611s] [PlayTest] [INFO] audio/ogg; codecs=opus,false,probably
[ 2.608s] [PlayTest] [INFO] audio/mpeg,true,probably
[ 2.605s] [PlayTest] [INFO] audio/mp4; codecs=mp4a.40.2,true,probably
[ 2.596s] [PlayTest] [INFO] audio/mp4; codecs=alac,false,false
[ 2.593s] [PlayTest] [INFO] audio/mp3,true,probably
[ 2.590s] [PlayTest] [INFO] video/matroska; codecs=opus,false,false
[ 2.587s] [PlayTest] [INFO] audio/flac,true,probably
[ 2.583s] [PlayTest] [INFO] audio/ape,false,false
[ 2.580s] [PlayTest] [INFO] audio/aiff,false,false
[ 2.577s] [PlayTest] [INFO] audio/aac,true,probably
[ 2.571s] [PlayTest] [INFO] START
```
