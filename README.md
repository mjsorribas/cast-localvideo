cast-localvideo
===============

Plays Local videos at your computer on your Chromecast. Beta for now.  

Requirements
============

1.	Chromecast on your network reachable, no client isolation in your router etc.
2. 	Chrome Browser version 32 or later
3. 	Cast extension in Chrome Store
4. 	NodeJS v0.10+
5. 	FFMpeg installed and reachable in PATH ([Windows guide](http://www.wikihow.com/Install-FFmpeg-on-Windows)) 
6.	A fast enough home interconnection network

How to install & use
====================

* 	On a terminal, do the following:

```

$ git clone https://github.com/mustafaakin/cast-localvideo.git
$ cd cast-localvideo
$ npm install
$ node app

```

* On your Chrome, go to address [http://localhost:8000](http://localhost:8000). You will see your folders (just change the folder to `/` on Linux & Mac. There is no root concept in Windows as it is in Unix, if you wish to use another drive, just use `D:` 

* Navigate through your folders to locate some video.
* Select the video and you will see the metadata if it is available in the file. (It currently shows all extensions, does not check if it is really a video file)
* Click play local to test if it plays on Chrome. Note that it plays very fast after some seconds, because Chrome cannot detect its length. It may be a bug, see this [Stackoverflow Question](http://stackoverflow.com/questions/21615089/http-header-for-duration-of-a-mp4-for-html-5-video) to help solving this. 
* Click Cast to Chromecast button to play the video on your Cast. It plays normally, at normal speed.
* Check the terminal if it gives any errors. Sometimes FFmpeg cannot handle the files and it crashes the application. *Sorry.*

Note
====

I developed this on Windows, on my parents computer remotely via TeamViewer. It is not feature complete, but it is easy to add features. Any pull requests & forks are welcome.  

TODOs
=====

1.	Be able to pause/resume content.
2.	Solve the [the duration bug](http://stackoverflow.com/questions/21615089/http-header-for-duration-of-a-mp4-for-html-5-video).
3.	Make use of session feature of Cast API to remember what is playing even if the server is down.
4.	Package it as a nice application for end users.
5.	Embed subtitles via FFMpeg.
6.	Resize the videos if they are too big.
7.	Options to change encoding options.

### Contact
Concatct *mustafa91* at *gmail* for any questions. And this is [my website](http://mustafaak.in)
