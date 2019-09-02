# ipad1-tvheadend-pi-tvhat
Project: repurpose the old Ipad 1st Gen as a TV viewer, thanks to Tvheadend and Pi TVHAT

**Limitations**
- Ipad 1st Gen is stuck on iOS 5.1
- It's a real pain to find and install suitable Apps for that iOS version.
- Video player app is really limited in term of video codecs and formats supported

**Good points**
- Hardware decoder for H264 videos *(only Quicktime can benefit from it)*
- Quicktime player can play MPEG-TS stream encoded with H264 (video) + AAC (audio)
- VLC is available (software decoder only, work great with MPEG2, doesn't work with H264)
- Nice screen *(while limited resolution)*
- The old Safari browser does support "vlc://" URL scheme to send video url to VLC and HTML5 Video element to send video url to Quicktime

--> So it could be suitable to watch TV on Ipad1 for both TNT "SD" (MPEG2) with VLC or TNT "HD" (H264) with Quicktime internal player *(need to re-encode on-the-fly the sound from AC3 to AAC)*.
For that Ipad1 would be the frontend/player, and the backend (aerial DVB-T TV receiver and streamer) would be done by [TVheadend](https://tvheadend.org/) on a Raspberry Pi equipped with [Pi TV HAT](https://www.raspberrypi.org/products/raspberry-pi-tv-hat/).

Then an interface to select channels and lunch the stream to player is needed...

On-the-fly re-encoding of the sound from AC3 to AAC takes up to 20% CPU on the Raspi 2.
