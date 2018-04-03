
# ffmpeg
```
https://zh.wikipedia.org/wiki/FFmpeg

組成元件:此計劃由幾個元件組成：
ffmpeg——一個命令列工具，用來對視訊檔案轉換格式，也支援對電視卡即時編碼
ffserver——一個HTTP多媒體即時廣播串流伺服器，支援時光平移
ffplay——一個簡單的播放器，基於SDL與FFmpeg函式庫
libavcodec——包含全部FFmpeg音訊/視訊編解碼函式庫
libavformat——包含demuxers和muxer函式庫
libavutil——包含一些工具函式庫
libpostproc——對於視訊做前處理的函式庫
libswscale——對於影像作縮放的函式庫
```
### lab 1:安裝ffmpeg
```
下載ffmpeg::https://www.ffmpeg.org/download.html#build-windows
點選Windows Packages Windows Builds即可下載
安裝如同一般Windows軟體安裝
```
### lab 2:認識ffmpeg

```
https://lnpcd.blogspot.tw/2012/09/ffmpeg.html

https://www.mobile01.com/topicdetail.php?f=510&t=3734550

在ffmpeg/bin目錄底下有三個.exe檔案

ffmpeg:

ffplay.exe:播放影片

ffprobe.exe:gathers information from multimedia streams and prints it in human- and machine-readable fashion.

ffprobe [options] [input_url]
 
it can be used to check the format of the container used by a multimedia stream and 
the format and type of each media stream contained in it.

If a url is specified in input, ffprobe will try to open and probe the url content. 
If the url cannot be opened or recognized as a multimedia file, a positive exit code is returned.

https://www.ffmpeg.org/ffprobe.html
http://zwindr.blogspot.tw/2016/08/tool-ffprobe.html
```
### 在cmd輸入ffmpeg 

```
ffmpeg version N-90433-g5b31dd1c6b Copyright (c) 2000-2018 the FFmpeg developers built with gcc 7.3.0 (GCC)
  configuration: --enable-gpl --enable-version3 --enable-sdl2 --enable-bzlib --enable-fontconfig --enable-gnutls 
  --enable-iconv --enable-libass --enable-libbluray --enable-libfreetype --enable-libmp3lame --enable-libopencore-amrnb 
   --enable-libopencore-amrwb --enable-libopenjpeg --enable-libopus --enable-libshine --enable-libsnappy --enable-libsoxr 
   --enable-libtheora --enable-libtwolame --enable-libvpx --enable-libwavpack --enable-libwebp --enable-libx264 --enable-libx265 
   --enable-libxml2 --enable-libzimg --enable-lzma --enable-zlib --enable-gmp --enable-libvidstab --enable-libvorbis 
   --enable-libvo-amrwbenc --enable-libmysofa --enable-libspeex --enable-libxvid --enable-libmfx --enable-amf --enable-ffnvcodec 
   --enable-cuvid --enable-d3d11va --enable-nvenc --enable-nvdec --enable-dxva2 --enable-avisynth
   
  libavutil      56. 12.100 / 56. 12.100
  libavcodec     58. 15.100 / 58. 15.100
  libavformat    58. 10.100 / 58. 10.100
  libavdevice    58.  2.100 / 58.  2.100
  libavfilter     7. 13.100 /  7. 13.100
  libswscale      5.  0.102 /  5.  0.102
  libswresample   3.  0.101 /  3.  0.101
  libpostproc    55.  0.100 / 55.  0.100
  
Hyper fast Audio and Video encoder

usage: ffmpeg [options] [[infile options] -i infile]... {[outfile options] outfile}...

Use -h to get full help or, even better, run 'man ffmpeg'
```
### 在cmd輸入ffmpeg -h
```
ffmpeg version N-90433-g5b31dd1c6b Copyright (c) 2000-2018 the FFmpeg developers built with gcc 7.3.0 (GCC)

  configuration: --enable-gpl --enable-version3 --enable-sdl2 --enable-bzlib --enable-fontconfig --enable-gnutls --enable-iconv --enable-libass --enable-libbluray --enable-libfreetype --enable-libmp3lame --enable-libopencore-amrnb --enable-libopencore-amrwb --enable-libopenjpeg --enable-libopus --enable-libshine --enable-libsnappy --enable-libsoxr --enable-libtheora --enable-libtwolame --enable-libvpx --enable-libwavpack --enable-libwebp --enable-libx264 --enable-libx265 --enable-libxml2 --enable-libzimg --enable-lzma --enable-zlib --enable-gmp --enable-libvidstab --enable-libvorbis --enable-libvo-amrwbenc --enable-libmysofa --enable-libspeex --enable-libxvid --enable-libmfx --enable-amf --enable-ffnvcodec --enable-cuvid --enable-d3d11va --enable-nvenc --enable-nvdec --enable-dxva2 --enable-avisynth
  
  libavutil      56. 12.100 / 56. 12.100
  libavcodec     58. 15.100 / 58. 15.100
  libavformat    58. 10.100 / 58. 10.100
  libavdevice    58.  2.100 / 58.  2.100
  libavfilter     7. 13.100 /  7. 13.100
  libswscale      5.  0.102 /  5.  0.102
  libswresample   3.  0.101 /  3.  0.101
  libpostproc    55.  0.100 / 55.  0.100

Hyper fast Audio and Video encoder

usage: ffmpeg [options] [[infile options] -i infile]... {[outfile options] outfile}...

Getting help:
-h      -- print basic options顯示基本選項
-h long -- print more options顯示更多選項
-h full -- print all options (including all format and codec specific options, very long)顯示所有選項
-h type=name -- print all options for the named decoder/encoder/demuxer/muxer/filter/bsf
See man ffmpeg for detailed description of the options.

Print help / information / capabilities:
-L                  show license
-h topic            show help
-? topic            show help
-help topic         show help
--help topic        show help
-version            show version
-buildconf          show build configuration
-formats            show available formats
-muxers             show available muxers
-demuxers           show available demuxers
-devices            show available devices
-codecs             show available codecs
-decoders           show available decoders
-encoders           show available encoders
-bsfs               show available bit stream filters
-protocols          show available protocols
-filters            show available filters
-pix_fmts           show available pixel formats
-layouts            show standard channel layouts
-sample_fmts        show available audio sample formats
-colors             show available color names
-sources device     list sources of the input device
-sinks device       list sinks of the output device
-hwaccels           show available HW acceleration methods

Global options (affect whole program instead of just one file:
-loglevel loglevel  set logging level
-v loglevel         set logging level
-report             generate a report
-max_alloc bytes    set maximum size of a single allocated block
-y                  overwrite output files
-n                  never overwrite output files
-ignore_unknown     Ignore unknown stream types
-filter_threads     number of non-complex filter threads
-filter_complex_threads  number of threads for -filter_complex
-stats              print progress report during encoding
-max_error_rate maximum error rate  ratio of errors (0.0: no errors, 1.0: 100% errors) above which ffmpeg returns an error instead of 
success.
-bits_per_raw_sample number  set the number of bits per raw sample
-vol volume         change audio volume (256=normal)

Per-file main options:
-f fmt              force format
-c codec            codec name
-codec codec        codec name
-pre preset         preset name
-map_metadata outfile[,metadata]:infile[,metadata]  set metadata information of outfile from infile
-t duration         record or transcode "duration" seconds of audio/video
-to time_stop       record or transcode stop time
-fs limit_size      set the limit file size in bytes
-ss time_off        set the start time offset
-sseof time_off     set the start time offset relative to EOF


-timestamp time     set the recording timestamp ('now' to set the current time)

-metadata string=string  add metadata

-program title=string:st=number...  add program with specified streams

-target type        specify target file type ("vcd", "svcd", "dvd", "dv" or "dv50" with optional prefixes "pal-", "ntsc-" or "film-")

-apad               audio pad

-frames number      set the number of frames to output

-filter filter_graph  set stream filtergraph
-filter_script filename  read stream filtergraph description from a file
-reinit_filter      reinit filtergraph on input parameter changes
-discard            discard
-disposition        disposition

Video options:(影片的相關選項)
-v frames number     set the number of video frames to output
-r rate             set frame rate (Hz value, fraction or abbreviation)
-s size             set frame size (WxH or abbreviation)
-aspect aspect      set aspect ratio (4:3, 16:9 or 1.3333, 1.7777)
-bits_per_raw_sample number  set the number of bits per raw sample
-vn                 disable video
-vcodec codec       force video codec ('copy' to copy stream)
-timecode hh:mm:ss[:;.]ff  set initial TimeCode value.
-pass n             select the pass number (1 to 3)
-vf filter_graph    set video filters
-ab bitrate         audio bitrate (please use -b:a)
-b bitrate          video bitrate (please use -b:v)
-dn                 disable data


Audio options:(聲音的相關選項)
-a frames number     set the number of audio frames to output
-aq quality         set audio quality (codec-specific)
-ar rate            set audio sampling rate (in Hz)
-ac channels        set number of audio channels
-an                 disable audio
-acodec codec       force audio codec ('copy' to copy stream)
-vol volume         change audio volume (256=normal)
-af filter_graph    set audio filters

Subtitle options:
-s size             set frame size (WxH or abbreviation)
-sn                 disable subtitle
-scodec codec       force subtitle codec ('copy' to copy stream)
-stag fourcc/tag    force subtitle tag/fourcc
-fix_sub_duration   fix subtitles duration
-canvas_size size   set canvas size (WxH or abbreviation)
-spre preset        set the subtitle options to the indicated preset
```
FFmpeg參數

```
FFmpeg可使用眾多參數，參數內容會根據ffmpeg版本而有差異，使用前建議先參考參數及編解碼器的敘述。
參數明細可用ffmpeg -h顯示；
編解碼器名稱等明細可用ffmpeg -formats顯示。

下列為較常使用的參數：

主要參數
-i——設定輸入檔名。
-f——設定輸出格式。
-y——若輸出檔案已存在時則覆蓋檔案。
-fs——超過指定的檔案大小時則結束轉換。
-t——指定輸出檔案的持續時間，以秒為單位。
-ss——從指定時間開始轉換，以秒為單位。
-t從-ss時間開始轉換（如-ss 00:00:01.00 -t 00:00:10.00即從00:00:01.00開始到00:00:11.00）。
-title——設定標題。
-timestamp——設定時間戳。
-vsync——增減Frame使影音同步。
-c——指定輸出檔案的編碼。
-metadata——更改輸出檔案的後設資料。
-help——檢視幫助資訊。

影像參數
-b:v——設定影像流量，預設為200Kbit/秒。（單位請參照下方注意事項）
-r——設定影格率值，預設為25。
-s——設定畫面的寬與高。
-aspect——設定畫面的比例。
-vn——不處理影像，於僅針對聲音做處理時使用。
-vcodec( -c:v )——設定影像影像編解碼器，未設定時則使用與輸入檔案相同之編解碼器。

聲音參數
-b:a——設定每Channel（最近的SVN版為所有Channel的總合）的流量。（單位請參照下方注意事項）
-ar——設定採樣率。
-ac——設定聲音的Channel數。
-acodec ( -c:a ) ——設定聲音編解碼器，未設定時與影像相同，使用與輸入檔案相同之編解碼器。
-an——不處理聲音，於僅針對影像做處理時使用。
-vol——設定音量大小，256為標準音量。（要設定成兩倍音量時則輸入512，依此類推。）

注意事項
以-b:v及-b:a偏好設定流量時，根據使用的ffmpeg版本，須注意單位會有kbits/sec與bits/sec的不同。（可用ffmpeg -h顯示說明來確認單位。）
例如，單位為bits/sec的情況時，欲指定流量64kbps時需輸入 -b:a 64k；單位為kbits/sec的情況時則需輸入 -b:a 64。
以-acodec及-vcodec所指定的編解碼器名稱，會根據使用的ffmpeg版本而有所不同。例如使用AAC編解碼器時，會有輸入aac與libfaac的情況。此外，編解碼器有分為僅供解碼時使用與僅供編碼時使用，因此一定要利用ffmpeg -formats確認輸入的編解碼器是否能運作。
```


### lab 2:使用ffplay播放本地端影片
```
ffplay 本地端影片
```
### lab 3:使用ffmpeg轉檔
```
ffmpeg -re -i Wildlife.wmv -vcodec h264 -b:v 1M -b:a 256k -s 720x576  3.mp4

參數說明::
```
### lab 4:使用ffmpeg錄製桌面轉並存成ts檔
```
ffmpeg -f GDIgrab -re -i desktop -vcodec h264 -b:v 1M -b:a 256k -s 720x576 -f mpegts 1.ts

參數說明::
```
### lab 5:使用ffmpeg錄製桌面並轉成udp直播串流
```
ffmpeg -f GDIgrab -re -i desktop -vcodec h264 -b:v 1M -b:a 256k -s 720x576 -f h264 udp://172.20.155.255:5555

參數說明::



參數設定:
```
