Android视频播放框架——封装FFMPEG的Vitamio

使用方法：
下载Vitamio的资源库 vitamio_lib,导入到工程中，使用提供的API.
在main清单文件中，关联Vitamiao的Activity
<activity android:name="io.vov.vitamio.activity.InitActivity"></activity>
    使用API和Android自带的VideoView相同，支持各种协议可以播放网络视频
    在使用的时候要判断硬件是否支持
if (!LibsChecker.checkVitamioLibs(this)) {return;}
		
		VideoView vv = (VideoView) findViewById(R.id.vv);
		
		vv.setVideoPath("sdcard/4.rmvb");
		vv.start();

在市面中有很多的第三方的控件，例如百度媒体云，github上的FFMPEG等

===============

Vitamio is an open multimedia framework for Android and iOS, with full and real hardware accelerated decoder and renderer.


New features
------------

Only few important features are listed here, we have fix many bugs and may introduce some new bugs.

1. The latest FFmpeg 2.0 git version, which should fix most playback issues, or bring some issues.
2. Support most FFmpeg AVOptions, which enables custom HTTP headers support.
3. Support more hardwares, e.g. X86 or MIPS.
4. Improve streaming, especially support adaptive bitrate streaming, you need open manually.
5. OpenSSL included, so some SSL related protocols, such as https, tls, rtmps, rtmpts, are supported.
6. Playback speed control from 0.5x to 2.0x.
7. Audio amplify to 2x volume.
8. Improved subtitle support, including external bitmap subtitles.
9. Cache online video to local storage and can be reused until you delete the cache file.
10. More MediaPlayer API, e.g. `getMetadata`, `getVideoTrack`.
11. The full Java code is open to all developers, modify and contribute is welcome.
12. Support RGBA\_8888 rendering, spport switching RGB\_565 or RGBA\_8888 to video rendering.
13. Enhance the hardware decoding in Android 16+.
14. Support ARMV6 CPU, may have some bugs.

How to use
----------

please see [the website](https://github.com/yixia/VitamioBundle/wiki)

License
-------

Please see [License](http://www.vitamio.org/en/License)


## Google+
Vitamio Developers Community on Google+ [http://goo.gl/fhCDTD](http://goo.gl/fhCDTD)
