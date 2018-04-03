
OBS 將遊戲實況同時播送至 Twitch、YouTube、LiveHouse

https://tedliou.com/archives/%E6%95%99%E5%AD%B8-obs-%E5%B0%87%E9%81%8A%E6%88%B2%E5%AF%A6%E6%B3%81%E5%90%8C%E6%99%82%E6%92%AD%E9%80%81%E8%87%B3-twitch%E3%80%81youtube%E3%80%81livehouse/


打開 Option.txt 這個檔案，修改檔案內容為以下格式
```
Twitch
push rtmp://live.twitch.tv/app/[串流金鑰]
Youtube
push rtmp://a.rtmp.youtube.com/live2/[串流金鑰]
LiveHouse
push rtmp://live-ea.livehouse.in/app/[串流金鑰]
Twitch 伺服器列表：http://bashtech.net/twitch/ingest.php
```

https://github.com/miaulightouch/nginx-rtmp-win32
