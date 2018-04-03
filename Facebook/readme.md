
# Facebook直播
```
如何使用直播串流軟體在 Facebook 進行直播？
https://www.facebook.com/help/587160588142067
```
### 桌上型播放軟體
```
Open Broadcaster Software(https://obsproject.com/)
Wirecast(要錢的)  https://www.telestream.net/wirecast/overview.htm
XSplit
```

## 在 Facebook 建立直播串流影片：
```
前往 https://www.facebook.com/live/create。
點擊建立直播串流影片。
選擇發佈直播的位置。
若要將串流金鑰設為永久有效，請選擇啟用持續性串流金鑰。若未選擇此選項，便無法在串流結束後再次使用此串流金鑰。
複製伺服器網址及串流金鑰（或持續性串流金鑰），並貼到串流軟體的設定中，然後從編碼器開始串流視訊。接著便會出現預覽畫面。
撰寫說明、標題及電玩遊戲標籤。
點擊開始直播或排程。

在軟體設定中輸入以下資訊。點選*安全連線（SSL）*
伺服器網址==>rtmps://live-api.facebook.com:443/rtmp/
```

## 步驟一:取得Facebook金鑰
1.使用自己帳號登入Facebook
2.進入創作者工作室
![Alt text][youtube_0.jpg]
3.點選即時串流
4.複製串流金鑰
步驟二:設定OBS
5.先在OBS來源中，點選+增加需要的畫面

==>我們這次選擇
顯示器擷取(當前電腦使用畫面)
視訊擷取裝置(camera)

6.點選設定 -> 串流==>選擇Youtube live==>然後把複製的金鑰貼上
步驟三:開始直播
7.在OBS中按下開始串流，剛剛打開的Youtube頁面就會出現了

8.按開始直播就好了
