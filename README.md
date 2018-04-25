# streaming 直播串流實戰

[facebook頻道](https://www.facebook.com/我的第一堂Linux-1798366720457828)
曾正好:myfirsthackingclub

[Youtube頻道](https://youtu.be/V8qGBgjsLpE)


#### 直播類型:內容當道
```
社交直播:A17
互動類直播：娛樂類互動，如YY等。
線上抓哇哇機:
機智問答直播:
HQ - Live Trivia Game Show
王思聰“既出錢又出力”支持的沖頂大會、映客直播的《芝士超人》、花椒直播的《百萬作戰》、今日頭條(西瓜視頻)的《百萬英雄》
諮詢直播:
教學直播:
商務直播:
金融類直播：金融直播可應用于即時解盤，線上專家講座，專家線上直播技術分析、指導投資者等使用場景。
大型賽事，演唱會類直播：可應用於大型演唱會，音樂會，遊戲，體育賽事等類直播場景。
會議類直播：大型會議直播。

```

## 直播劇本

```
好劇本讓你的影片打遍天下無敵手，從《艾倫脫口秀》看劇本架構
https://www.inside.com.tw/2017/07/04/lesson-learned-from-ellen-show

http://bbs.tianya.cn/post-384-37609-1.shtml
```
## week1:VLC串流伺服器與ffmpeg
```
lab1:安裝與建置VLC串流伺服器
    https://zh.wikipedia.org/wiki/VLC多媒體播放器
    https://www.videolan.org/vlc/index.zh-TW.html
lab2:使用VLC播放已錄製的影片+使用VLC觀看影片
lab3:使用VLC播放串流影片+使用VLC觀看影片
lab4:使用obs播放串流影片到VLC串流伺服器++使用VLC觀看影片++使用手機觀看影片
```
```
lab5:使用ffmpeg播放直播
lab6:ffmpeg錄影並直播到串流伺服器

### nginx rtmp直播伺服器
(1)nginx rtmp@linux
nginx-rtmp-module，組合在一起即可以搭建一個功能相對比較完善並可支援RTMP和HLS的流媒體伺服器。

(2)用ffmpeg產生一個模擬直播源，向rtmp伺服器推送
ffmpeg -re -i test.flv -f flv rtmp://192.168.242.172/myapp/test1
ffmpeg -re -i Caminandes.mp4 -vprofile baseline -vcodec copy -acodec copy -strict -2 -f flv rtmp://192.168.242.172/myapp/test2

(3)使用ffplayer或者vlc播放rtmp流
ffplay rtmp://192.168.242.172/myapp/test1

### 實況聊天室的統一大業：使用 MULTICHAT
http://upsetlink.logdown.com/bullshit/425985
```
## week2:手機直播與PC直播

### live直播:

### PC直播:obs==>Youtube/Facebook
```
建立Youtube直播
您可以透過下列 4 種方式中的任一種來建立 YouTube 直播。
(1)立即直播  (2)活動  (3)行動裝置  (4)網路攝影機

Youtube影片設置浮水印:https://bearteach.com/bearman/537
```
```
PC直播軟體:belive | Ecamm live | OBS Studio

OBS官網 : https://www.obsproject.com/
【使用OBS實況 Twitch直播教學】皮克小教室 第一集:https://www.youtube.com/watch?v=PI25SbWVSNU
【使用OBS實況 編輯場景教學 圖片新增 修改比例】皮克小教室 第二集:https://www.youtube.com/watch?v=cLTIaV7N5Ks
【OBS Studio 工作室版本 詳細介紹 】皮克小教室第二季 第一集:https://www.youtube.com/watch?v=aBsAISxDxww
【Streamlabs 追隨訂閱Donate 介紹 】皮克小教室第二季 第二集:https://www.youtube.com/watch?v=uEVQVHr38ag
【REVLO 介紹 】皮克小教室第二季 第三集:https://www.youtube.com/watch?v=p-az6vFRPso
【弒可樂】OBS文字跑馬燈、聊天室去背、訂閱斗內顯示 + 串流編碼設定教學:https://www.youtube.com/watch?v=B1dJ8O6AZRw&t=30s

【諳石實況】系列
OBS Studio 最新版 設定教學 #1 :https://www.youtube.com/watch?v=PPKlihiwYVs
youtube+obs直播串流教學:https://www.youtube.com/watch?v=fp-ShffMgcw

```

### 手機直播:圓剛《Live in Five》

《Live in Five》
```
《Live in Five》Android版|iOS版載點:
https://www.avermedia.com/tw/tv_more/product/streaming_capture/live_in_five

手機平板的直播APP～live in five:https://www.youtube.com/watch?v=5v6F1RYwHGs

lab:iOS手機BeLive.tv->facebook->VLC
https://itunes.apple.com/us/app/belive-tv/id1139884068?mt=8```
```
### IOS直播==>Youtube/Facebook
```
Livestream(IOS)

https://itunes.apple.com/us/app/livestream/id493086499?mt=8
```
### Android 直播==>Youtube/Facebook

## week3: 期中報告
### Nginx直播實務
```
[1]Nginx@windows
在Windows下搭建基于nginx的视频直播和点播系统
https://my.oschina.net/gaga/blog/478480

[2]Nginx@linux
基於Nginx搭建RTMP/HLS視頻直播伺服器:
https://www.jianshu.com/p/0296a7be7928

http://gitbook.cn/books/595754c2a13db23ff231ec7c/index.html

Nginx的擴展rtmp模組
github：https://github.com/arut/nginx-rtmp-module

```
### 多平台同步直播實務
```
使用Nginx 
http://upsetlink.logdown.com/bullshit/425541
https://bearteach.com/bearman/14
```

### 雲端Nginx直播實務
```
Amazon
http://blakew88.blogspot.tw/2017/04/rtmp13-nginx-rtmp.html
http://blakew88.blogspot.tw/2017/04/rtmp23-nginx-hls.html

Azure
使用 MICROSOFT AZURE MEDIA SERVICE 建立直播服務
http://blakew88.blogspot.tw/2017/04/microsoft-azure-media-service.html
```


```
遊戲直播
直播軟體: XSplit 
直播平台: https://www.twitch.tv/broadcast
```
## week4:進階直播專題(HTTP/RTSP)

###  Red5 
```
GitHub:https://github.com/Red5/red5-server 
http://gitbook.cn/books/595754c2a13db23ff231ec7c/index.html
```
###  WebRTC Live Streaming直播實務
```
Low Latency WebRTC Live Streaming - Open Source Ant Media Server
https://antmedia.io/
https://github.com/ant-media/Ant-Media-Server
```

### 攝影機+重裝備播(影像擷取卡+ffmpeg)

## week5:戶外直播實戰

### 三軸穩定器的使用{不教單眼|只用手機}

## week6: 期末報告 streaming 直播串流實戰作業:
```
作業2:名人訪問直播==>系主任
作業3:搞笑直播
作業4:拍賣直播
作業5:教學直播
```


# streaming 直播串流周邊設播

http://news.ltn.com.tw/news/consumer/paper/1086410

#### 手持穩定器三軸穩定器::DJIO SMO Mobile
```
操作穩定之外，最大的特色是軟硬體整合相當完整，例如超廣角全景、智慧跟隨模式與聰明的移動延時攝影功能
強調軟硬體整合性 DJI OSMO Mobile 三軸穩定器::
https://www.mobile01.com/newsdetail/20085/dji-osmo-mobile-three-axis
DJI Osmo Mobile:三軸穩定器，除了黑色，另為女性族群推出銀色款。
搭配專用App，具備人臉智慧追蹤、美顏功能。售價11,200元，先創國際官網。
```
#### 飛宇SPG Live 360°:三軸穩定器，人體工學手柄，握持舒適度高。
```
不管橫拍、直拍都能用，續航力約8小時。售價7,990元
開箱 | CP值最高穩定器?! 手機專用SPG三軸穩定器:https://www.youtube.com/watch?v=MUCU6f5112I
2018 版 SPG C 、 SPG 三軸穩定器搭配運動相機手機打補帖 1  https://www.youtube.com/watch?v=WrURD33XCeE
2018 版 SPG C 、 SPG 三軸穩定器搭配運動相機手機打補帖 2  https://www.youtube.com/watch?v=8E4yZSjLpQk

怪機絲 大 三軸穩定器 大PK A2000 、 MG Lite 、 Crane 2 、 KD2600 GBRA 胸器 省力裝置 教學 優缺點分析
https://www.youtube.com/watch?v=6phO1HK_O6M
```
#### 《手持穩定器》SwiftCam Hello Kitty

外型超萌的Hello Kitty二軸穩定器，整體配色為白色搭配粉紅色。可折疊設計，方便攜帶。售價4,680元

#### 《站立式腳架》
```
便攜式相機手機自拍四節輕型三腳架★ 附贈手機架，相機/手機一支腳架可搞定 
★ 重量極輕，僅350克 ★ 體積小巧，收納好輕鬆 ★ 4種高度可調整，拍出完全角度 

手機藍牙自拍桿二合一三腳架(VCT-1688)

Manfrotto MKCOMPACTADV COMPACT系列五節腳架/165cm

AISURE 直播神器 360度旋轉手機相機兩用腳架(附收納袋)
```
#### 《桌上型腳架》適用手機還是單眼要確定
```
Manfrotto PIXI SMART(MKPIXICLAMP)輕巧迷你腳架，附有萬用手機夾，適用市面多數手機。
Manfrotto PIXI EVO進階迷你腳架:https://www.youtube.com/watch?v=kejrLTD6PjE
```
#### Xenomix手機架:高彈力彎夾設計，加入防滑塗層，能360度旋轉改變支架方向。亦能使用在自行車上。

#### MeFOTO MK10:自拍棒結合桌上型腳架，底部加入防滑設計，可兼容手機和Gopro。

#### Kamera 佳美能 Smile-360 三腳架自拍棒直播架(藍牙版)-黑色

#### 手機收音: (1)手機  (2)耳機 SAMSUNG S5手機送  (3)指向麥克風 鐵三角 AT9913iS

#### 專業USB電容錄音麥克風
```
Blue Raspberry 全裝置USB麥克風
號稱是市場唯一可隨身帶著走的電容式麥克風，可連結電腦或手機使用，隨插即用。售價7,800元

http://24h.pchome.com.tw/prod/DPAH4J-A9007PWKL?q=/S/DPAH4J

ALCTRON UM100 專業USB電容錄音麥克風 
```
#### 特殊鏡頭
```
【魚眼+廣角+微距 三合一鏡頭!!】 萬用手機平板鏡頭夾 光學玻璃鏡頭
```
#### 美顏補光燈
```
LIEQI LQ-035 內建10顆LED燈，提供3段補光效果，另結合微距、廣角拍攝功能。原價899元，特價489元，PChome 24h購物。
多功能手機補光燈化妝鏡 RK16:自拍補光燈/手機支架/附收納包/直播神器/自拍神器/美白/美顏/美肌/打光
```
# 直播軟體: 

## IOS手遊直播:獅吼、Omlet Arcade、shou、Mobcrush
```
https://home.gamer.com.tw/creationDetail.php?sn=3567494
https://www.mobile01.com/topicdetail.php?f=383&t=5258533

Omlet Arcade 支援 iOS 11，一鍵直播遊戲畫面至Facebook, YouTube, Twitch 和Omlet
https://www.youtube.com/watch?v=eNad1ZVA_NY
```

## Android手遊直播:shou、Omlet Arcade、YouTube Gaming
```
YouTube Gaming 手機版APP│直播實況:https://www.youtube.com/watch?v=LfrhjHlP7TY

Android 手遊直播APP比較(Youtube gaming、Twitch、Soocii) - 巴哈姆特手機版
https://m.gamer.com.tw/home/creationDetail.php?sn=3842984
```

# 雲端streaming串流伺服器

YouTube Live: https://www.youtube.com/channel/UC4R8DWoMoI7CAwX8_LjQHig


# streaming串流伺服器

### nginx rtmp直播伺服器
```
(1)nginx rtmp@linux
nginx-rtmp-module，組合在一起即可以搭建一個功能相對比較完善並可支援RTMP和HLS的流媒體伺服器。

(2)用ffmpeg產生一個模擬直播源，向rtmp伺服器推送
ffmpeg -re -i test.flv -f flv rtmp://192.168.242.172/myapp/test1
ffmpeg -re -i Caminandes.mp4 -vprofile baseline -vcodec copy -acodec copy -strict -2 -f flv rtmp://192.168.242.172/myapp/test2

(3)使用ffplayer或者vlc播放rtmp流
ffplay rtmp://192.168.242.172/myapp/test1

```
# Top 19 Free Movie Streaming Apps for iPad

https://www.iskysoft.com/mobile-tips/free-movie-streaming-apps-for-ipad.html

https://itunes.apple.com/us/app/17live-best-live-streaming-app/id988259048?mt=8
