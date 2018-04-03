
# Facebook直播
```
如何使用直播串流軟體在 Facebook 進行直播？
https://www.facebook.com/help/587160588142067

如何在 Facebook 進行現場直播？
https://www.facebook.com/help/1636872026560015?helpref=faq_content
```
### 桌上型播放軟體
```
Open Broadcaster Software(https://obsproject.com/)
Wirecast(要錢的)  https://www.telestream.net/wirecast/overview.htm
XSplit
```

## 在 Facebook 建立直播串流影片：
```
https://www.facebook.com/help/587160588142067

前往 https://www.facebook.com/live/create。
點擊建立直播串流影片。
選擇發佈直播的位置。
若要將串流金鑰設為永久有效，請選擇啟用持續性串流金鑰。若未選擇此選項，便無法在串流結束後再次使用此串流金鑰。
複製伺服器網址及串流金鑰（或持續性串流金鑰），並貼到串流軟體的設定中，然後從編碼器開始串流視訊。接著便會出現預覽畫面。
撰寫說明、標題及電玩遊戲標籤。
點擊開始直播或排程。

在軟體設定中輸入以下資訊。點選*安全連線（SSL）*
伺服器網址(使用443 port)==>rtmps://live-api.facebook.com:443/rtmp/

在軟體設定中輸入以下資訊。沒點選*安全連線（SSL）*
伺服器網址(使用80 port)==>rtmp://live-api.facebook.com:80/rtmp/

```

## 步驟一:取得Facebook金鑰


## 步驟二:設定OBS
```
先在OBS來源中，點選+增加需要的畫面

==>我們這次選擇
顯示器擷取(當前電腦使用畫面)
視訊擷取裝置(camera)

.點選設定 -> 串流==>選擇Youtube live==>然後把複製的金鑰貼上
```

## 步驟三:開始直播

7.在OBS中按下開始串流，剛剛打開的頁面就會出現了

8.按開始直播就好了
