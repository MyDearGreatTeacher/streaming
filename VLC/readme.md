# ref
```
http://www.arthurtoday.com/2012/09/vlc-player-streaming-video-server.html

http://blog.xuite.net/yh96301/blog/47629906-%E5%85%8D%E8%B2%BB%E5%BD%B1%E9%9F%B3%E6%92%AD%E6%94%BE%E8%BB%9F%E9%AB%94VLC+media+player

VLC Media Player是一款免費、開放程式碼、跨平台、中文化、畫面簡潔沒有廣告、
功能強大的影音播放軟體，支援藍光、DVD/VCD、MKV、FLV、WMV、MPEG1、MPEG2、
MP4、DivX、MP3、OGG、AVI、RM、MOV、FLAC、APE…等大多數的影音檔案，
目前已經更新為3.0版。
它可以在輸入影音網站網址後直接播放線上串流影音，
還能用來預覽eMule/BT未下載完成的影片檔案，
讓您能先欣賞影片的類型或清晰度是否符合您的需求；
播放DVD沒有區碼的限制，可以跳過版權宣告和廣告片段直接欣賞影片，
播放影片十分順暢，占用系統資源很小，是一款非常好用的影音播放軟體。


使用VLC Media Player播放影音檔案，外掛字幕或播放清單編碼必須使用UTF-8，才能正確顯示中文字型，
轉換編碼的方法參考：VLC media player外掛字幕顯示亂碼。

http://www.arthurtoday.com/2012/09/vlc-player-streaming-video-server.html


VLC media player重複播放。
VLC media player錄製影片。
VLC media player擷取畫面。
VLC media player切換語言與字幕。
VLC media player外掛字幕顯示亂碼。
VLC media player轉換YouTube影片
```
### 安裝
```
下載:: https://www.videolan.org/vlc/index.zh_TW.html

linux: 
sudo apt-get install ffmpeg
sudo apt-get install vlc

Windwos:連結到官方網站，點選「Instaler for 64bit version」，下載64位元的版本。
直接點選「下載 VLC」，可以下載32位元的版本。
```
啟動後，請點選右上方的「媒體」選單，然後，再點選「串流(S)」項目

跳出「選擇檔案」的視窗，請點選「加入」按鈕來選擇你要在串流播放出去的檔案
可以多選，到時候可以連續播放的哩 ! 
選好之後，請點選下方的「串流(S)」按鈕。

跳出「串流輸出」的視窗，請點選下方的「目的地設定」大按鈕，
按完後，會接著出現「目的地」設定視窗。

在「目的地」設定視窗的新目的地項目右邊的下拉選單選擇「HTTP」後，
點選右方的「加入」按鈕來進入 「HTTP」 的設定畫面，
另外，預設的情況下，負責串流放送影片的這台電腦是不播出影片的，
如果要播出影片，就要勾選「本機顯示」這個項目哩！

「HTTP」 設定畫面的項目都可以不用調整，除非是要有需要改變「連接埠」，否則，建議是採用預設值就可以了哩 

接下來，只要點選下方的「串流」按鈕就會開始播放了哩

```
### 使用 VLC 架設串流伺服器
```
Fork from http://albert-oma.blogspot.tw/2014/01/vlc.html

使用 VLC 架設串流伺服器
以下使用文字記錄使用VLC來當成串流伺服器的操作過程。
喜歡看圖的可以參考 William.L 所整理的SlideShare
https://www.slideshare.net/wiliwe/streaming-media-server-setup-manual

1. 安裝 VLC 
sudo apt-get install ffmpeg
sudo apt-get install vlc

2. 設定使用 http 進行串流
[媒體] -> [stream]
[開啟媒體] -> [檔案] -> [增加] 欲串流的檔案後，選擇[串流]
[來源] 直接選擇 [Next]
[Destination Setup] -> New destionation 改為 HTTP, 選擇 [Next], 按下增加
[Transcoding Options] -> 取消 Activate Transcoding，
針對不同bitrate需要新增不同的設定檔案，以256kb為例，設定檔內容如下：
Encapsulation：MP4/OOV
視訊編碼器：H-264, bitrate: 256kb/s, 其他維持不變
音訊編碼器：MPEG Audio, bitrate 12kb/s, channel 1, sample rate 8000
此時回到 VLC 主畫面，直接進行播放。
遠端的 Client 可以使用 http://vlc-streaming-server-ip:8080/ 進行連線

3. 設定使用 RTSP 進行串流
a. RTSP over UDP 的設定
基本設定
vlc -vvv 140000.mp4 --sout '#rtp{sdp=rtsp://192.168.0.169:8080/test.sdp}'

動態降低 bitrate 至 64kbits (需安裝ffmpeg與libavcodec)
vlc -vvv 140000.mp4 --sout 
'#transcode{vcodec=h264,vb=64,scale=1,acodec=mp4a,ab=12,channels=1,samplerate=8000}:rtp{sdp=rtsp://192.168.0.169:8080/test.sdp}'

將 input stream 降低 bitrate 後，讓 vlc client 進行連線
vlc -vvv rtsp://192.168.0.2:554/livestream --sout '
#transcode{vcodec=h264,vb=64,scale=1,acodec=mp4a,ab=12,channels=1,samplerate=8000}:rtp{sdp=rtsp://192.168.0.169:8080/test.sdp}'

b. 根據不同的bitrate，設定多個 streaming，提供使用者動態選擇

b1. 先透過 GUI, 設定 VLC 支援 telnet interfcae，記得要設定密碼
b2. 設定 vlm.conf 如下

################
# rtsp streams #
################ 
# Use below command to execute this script
# vlc -vvv --color --vlm-conf vlm.conf --rtsp-host 192.168.0.169 --rtsp-port=8080

BloggerAds 部落格行銷
# Use below url to connect to VLC Stream server
# rtsp://192.168.0.169:8080/TEST_512 
new Stream1 vod enabled
new Stream1 vod enabled

setup Stream1 input video1.mp4
setup Stream2 input video2.mp4

setup Stream1 output
setup Stream2 output

b3. 啟動 VOD(Video On Demand) 服務  
vlc -vvv --color --vlm-conf vlm.conf --rtsp-host 192.168.0.169 --rtsp-port=8080 
b4. client 要求 streaming 
使用 URL rtsp://192.168.0.169:8080/TEST_512 進行連線

參考資料
手動安裝 libavcodec
http://askubuntu.com/questions/13737/what-packages-do-i-install-for-ffmpeg-and-libmp3lame
http://ubuntuforums.org/showthread.php?t=786095][1]   
VLC command line 命令查詢
http://www.videolan.org/doc/streaming-howto/en/ch03.html   
https://wiki.videolan.org/VLC_command-line_help
一個vod 的例子
http://people.videolan.org/~dionoea/vlc-plugin-demo/serversetup.php
```

