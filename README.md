#### DASH-Video Source code
##### Dash.js
- 基于dash.js的视频播放器
- 访问的index位于```/videoplayer/3(or 1)/index.html```
- 改进算法在```/videoplayer/3/app/rules/DownloadRatioRule.js```体现
- 没有提供source video，如需要需要在和dash.js同级的目录下新建一个video_src文件夹，其中还需要建立视频编号1/3的子文件夹，该文件夹中需要存放dash.js接受的文件类型（MPD及分段MP4），生成方式即cut.sh所描述的命令行

##### cut.sh
- 切片指令 其中video.mp4参数可以换成相应的视频源文件名

##### live
- 直播部分的服务器搭建和推流等操作，详见live中的README.txt

##### dash-video & Openwebsite.sh
- 基于vue.js的项目主页
- 需要npm编译后才能使用，详见Openwebsite.sh和dash-video中的README.md
- 在打开网站前需要先修改dash-video/src/components/watchvideo.vue中视频的URL和livevideo.vue中直播源的URL为服务器上正确的地址才能正常链接到点/直播服务器和视频源。