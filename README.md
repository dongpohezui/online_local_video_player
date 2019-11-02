# 在线本地视频播放器

## 概述
通过在线网页播放本地下载好的视频


## 待改进
1. html5支持的视频格式有限
当前， \<video> 元素支持三种视频格式： MP4, WebM, 和 Ogg:

| 浏览器	  |         MP4	         | WebM	 |  Ogg  |
| ---------- | --------------------- | ------ | ----- |
| Internet  Explorer | YES	  | NO	 | NO	 |
| Chrome	 | YES	                 | YES	  | YES   |
| Firefox	 | YES	                 | YES	  | YES   |
| Safari	 | YES	                 | NO	  | NO    |
| Opera	     | YES (从 Opera 25 起)	 | YES	  | YES   |

MP4    = 带有 H.264 视频编码   和 AAC 音频编码的 MPEG 4 文件

WebM = 带有 VP8 视频编码      和 Vorbis 音频编码的 WebM 文件

Ogg    = 带有 Theora 视频编码  和 Vorbis 音频编码的 Ogg 文件

可以通过js扩展其支持的视频格式，比如flv.js

2. 播放器控件编写及界面的优化

## 常见问题
### 有很多优秀的本地视频播放器软件，为什么要用浏览器播放？
1. 不想为了看视频而去下载新的软件
2. 用浏览器播放会有一些有趣的功能，比如谷歌浏览器播放视频最快可以达到16倍速

### 浏览器直接可以播放视频，为什么要写一个网页？
1. html5播放器支持的视频格式有限，但是可以通过js扩展其支持的视频格式有限，比如flv.js
2. just for fun

### 目前播放本地视频的时候使用的是什么播放器？
迅雷内置的播放器XMP.exe

好处是不用下载新的软件，不足是不支持倍速播放

参考链接：哪个视频播放器好？ - 知乎
https://www.zhihu.com/question/20033434




## 代码编写
### \<vidoe>
### playbackRate
playbackRate 属性设置或返回音频/视频的当前播放速度

例值：
1.0 正常速度
0.5 半速（更慢）
2.0 倍速（更快）
谷歌浏览器最高支持16倍速播放

### 常用API
常用的一些 video API

"视频播放":video.play();

"视频暂停播放":video.pause();

"视频地址":video.currentSrc;

"视频总时长":video.duration;

"视频播放速率":video.playbackRate;

"是否暂停":video.paused;

"是否结束":video.ended;

"是否静音":video.muted;  

"当前播放时间": video.currentTime;

"当前缓冲量":video.buffered.end(0);

"当前音量":video.volume

