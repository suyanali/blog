---
aliases: []
title: 字幕_語音轉文字+翻譯(google ai studio)自動化
tags: [未分類]
categories: 未分類
date: 2025-06-18T08:55:26
modified: 2025-06-18T16:49:09
draft: false
toc: true
---

建立時間: 2025-06-18T08:55:26

最後修改日: 2025-06-18T08:55:26

tags:  #未分類

---
# 字幕_語音轉文字+翻譯(google ai studio)自動化
---

---

>[!SUMMARY]+ Table of Contents
>- [字幕_語音轉文字+翻譯(google ai studio)自動化](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#字幕_語音轉文字+翻譯(google%20ai%20studio)自動化)
>    - [原則： 影片轉音檔並切割→依序上傳google ai studio(沒處理好就多問幾次)、下載→整理+合併srt檔](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#原則：%20影片轉音檔並切割→依序上傳google%20ai%20studio(沒處理好就多問幾次)、下載→整理+合併srt檔)
>    - [流程概述：](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#流程概述：)
>    - [重要：](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#重要：)
>    - [準備：](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#準備：)
>    - [步驟](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#步驟)
>        - [(1)影片切割並轉存wav/mp3](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#(1)影片切割並轉存wav/mp3)
>            - [1.先安裝ffmepg並設定path(參考網路教學，path位置請依據自己電腦設定)](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#1.先安裝ffmepg並設定path(參考網路教學，path位置請依據自己電腦設定))
>            - [2.bat自動化使用ffmepg指令切割影片並轉成音檔](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#2.bat自動化使用ffmepg指令切割影片並轉成音檔)
>                - [**--有興趣也可以照以下步驟自己建立--**](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#**--有興趣也可以照以下步驟自己建立--**)
>            - [3.(可有可無)批次變更檔名](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#3.(可有可無)批次變更檔名)
>        - [(2)分割後影片上傳google ai studio](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#(2)分割後影片上傳google%20ai%20studio)
>            - [**1.到google ai studio網站**](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#**1.到google%20ai%20studio網站**)
>            - [**2.選擇上傳檔案**](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#**2.選擇上傳檔案**)
>            - [**3.找到audio_parts裡音檔，只上傳"一個"**](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#**3.找到audio_parts裡音檔，只上傳"一個"**)
>            - [**4.輸入指定prompt，跟音檔一起Run**](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#**4.輸入指定prompt，跟音檔一起Run**)
>            - [**5.確認生成的srt是否符合格式以及是否有翻譯成繁體中文**](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#**5.確認生成的srt是否符合格式以及是否有翻譯成繁體中文**)
>            - [**6.字幕檔達標準就可以下載下來，副檔名直接用.srt儲存，小錯誤字幕軟體能自動修正**](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#**6.字幕檔達標準就可以下載下來，副檔名直接用.srt儲存，小錯誤字幕軟體能自動修正**)
>                - [●ai常見錯誤1:](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#●ai常見錯誤1:)
>                - [●ai常見錯誤2:](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#●ai常見錯誤2:)
>                - [●ai常見錯誤3:](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#●ai常見錯誤3:)
>        - [(3) srt檔加入開頭、末端標記，使未來合併字幕好自動對齊時間軸](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#(3)%20srt檔加入開頭、末端標記，使未來合併字幕好自動對齊時間軸)
>                - [**--有興趣也可以照以下步驟自己建立--**](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#**--有興趣也可以照以下步驟自己建立--**)
>        - [(4)合併字幕並對齊時間軸](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#(4)合併字幕並對齊時間軸)
>                - [**--有興趣也可以照以下步驟自己建立--**](字幕_語音轉文字+翻譯(google%20ai%20studio)自動化.md#**--有興趣也可以照以下步驟自己建立--**)

---

---
---
1. prompt來自 https://www.threads.com/@prompt_case/post/DKzLVCFNs5q?xmt=AQF01KiCGxQliy_xilEupl8-J0qEe8X5qY3SA6wak9Ja7w
2. 文章同步發布於: https://github.com/suyanali/blog/blob/main/Other/%E5%AD%97%E5%B9%95_%E8%AA%9E%E9%9F%B3%E8%BD%89%E6%96%87%E5%AD%97%2B%E7%BF%BB%E8%AD%AF(google%20ai%20studio)%E8%87%AA%E5%8B%95%E5%8C%96.md
3. 可搭配教學影片服用: https://youtu.be/pXxUNgjT9pc
---
## 原則： 影片轉音檔並切割→依序上傳google ai studio(沒處理好就多問幾次)、下載→整理+合併srt檔
用什麼方式切割或合併字幕檔都可以，依自己習慣。

我提供的是我自己試驗的方式
## 流程概述：
先將影片檔切割成每10分鐘一段(最好轉成音檔，上傳速度會比較快)

→將音檔(例如0.wav)上傳google ai studio，並輸入指定prompt(1)等待結果

→初略檢查有沒有翻成中文以及Srt格式是否正確，若否則輸入指定prompt(2)修正

→ok後下載下來，副檔名直接填.srt。

→在電腦還是得再次檢查srt格式，著重在第一行有無正確，若不正確

→打開字幕軟體(例如subtitle edit)，開啟該字幕檔，並按儲存，確保整份srt格式正確，我一般會在這時順便快速檢查有無字幕出現不正常超長停留秒數(軟體會有橘底標示)，順便改掉

→再來重新整理google ai studio網頁(=開新的chat)，重複步驟，上傳，檢查格式，下載。直到都翻譯完。

→每個srt檔插入抬頭結尾做標記

→所有字幕合併，並且修正時間軸

→最後打開字幕軟體(例如subtitle edit)，開啟該合併字幕檔做最後確認。

以上有幾個步驟有程式可以自動化

以下操作使用google ai studio免費版、windows電腦

## 重要：
1. 影片一定要切10分鐘以內，10min以上依照經驗會跑不出後面結果或轉圈圈很久。轉成音檔上傳最好
2. 用完記得定期到google雲端找google ai studio資料夾，把裡面剛上傳的檔案刪掉+清理垃圾桶喔
3. 每次ai生成的字幕檔一定一定要檢查srt格式!!，以免合併字幕檔時時間軸不對，或漏了

## 準備：
1. 安裝ffmepg並設定PATH [(教學)](https://ivonblog.com/posts/yt-dlp-installation/)
2. 安裝python並設定好PATH [(教學)](https://www.pcschool.com.tw/blog/it/python-installation)以及撰寫python的介面，介面我都用簡單的記事本軟體[notepad++](https://notepad-plus-plus.org/downloads/)解決
3. 安裝字幕軟體，例如[subtitle edit](https://www.nikse.dk/subtitleedit)
4. 一個google帳號
5. 準備翻譯的影片
6. (可要可不要) 批次編輯檔名程式，例如[ReNamer](https://www.den4b.com/products/renamer)
7. 將 [這裡的](https://mega.nz/file/kNE33KoI#l42c7eHxPiOlK0iZbiPuv_ki0e3rfrhbqpLsEIxwY-o) 3個bat檔跟1個python檔下載，等下會用到 (你也可以自己建)
   
   3個bat檔跟1個python檔下載: https://mega.nz/file/kNE33KoI#l42c7eHxPiOlK0iZbiPuv_ki0e3rfrhbqpLsEIxwY-o

## 步驟
### (1)影片切割並轉存wav/mp3
#### 1.先安裝ffmepg並設定path(參考網路教學，path位置請依據自己電腦設定)
![Imgur](https://i.imgur.com/DkJEuEn.png)

#### 2.bat自動化使用ffmepg指令切割影片並轉成音檔

依據原始影片是mkv或mp4跑不同程式，若有其他需求可以讓chatgpt幫你改，該程式功能為將這個資料夾裡的影片轉成音檔並以每10分鐘分割。

`可以直接使用我提供的"split_audio_10min_mkv.bat"(for MKV格式)或"split_audio_10min_mp4.bat"(for mp4格式)`


將bat放到與目標影片同一資料夾，要轉的影片記得只放<span style="background:#fff88f">1個</span>!!!

![Imgur](https://i.imgur.com/WiZ6fUQ.png)

本例為mkv檔，直接雙擊MKV轉wav那個bat(我命名為split_audio_10min_mkv.bat)，可以看到命令窗口在跑，等待他跑完

![Imgur](https://i.imgur.com/f4blgIg.png)

跑完圖如下，會出現「請按任意鍵繼續」

![Imgur](https://i.imgur.com/EBm1Jnx.png)


分割的音檔都在audio_parts資料夾裡

![Imgur](https://i.imgur.com/Wa5HWX4.png)
##### **--有興趣也可以照以下步驟自己建立--**

先開啟一個空白筆記本，將以下code貼上並存檔，副檔名記得刪除.txt並改成.bat
![Imgur](https://i.imgur.com/ZvvYQUH.png)


此為MKV轉wav
```bat
@echo off
setlocal enabledelayedexpansion

REM 建立輸出資料夾
if not exist "audio_parts" mkdir audio_parts

REM 處理所有 mkv 檔
for %%F in (*.mkv) do (
    echo 處理檔案：%%F
    ffmpeg -i "%%F" -vn -acodec pcm_s16le -ar 16000 -ac 1 -f segment -segment_time 600 -reset_timestamps 1 "audio_parts\%%~nF_%%03d.wav"
    echo 完成 %%F
)

echo 全部完成！
pause

```

此為MP4轉mp3
```bat
@echo off
setlocal enabledelayedexpansion

REM 建立輸出資料夾
if not exist "audio_parts" mkdir "audio_parts"

REM 處理所有 mp4 檔
for %%F in (*.mp4) do (
    echo 處理檔案：%%F
    ffmpeg -i "%%F" -vn -acodec libmp3lame -ab 192k -ar 44100 -ac 2 -f segment -segment_time 600 -reset_timestamps 1 "audio_parts\%%~nF_%%03d.mp3"
    echo 完成 %%F
)

echo 全部完成！
pause

```

--步驟1-2結束--

#### 3.(可有可無)批次變更檔名

因為檔名太長了(我不好快速分辨)，使用批次改檔名方式改，或手動改，或者在一開始影片名稱就不要那麼長
![Imgur](https://i.imgur.com/NaMP9Js.png)
### (2)分割後影片上傳google ai studio
#### **1.到google ai studio網站**

#### **2.選擇上傳檔案**

![Imgur](https://i.imgur.com/bV24KnM.png)

#### **3.找到audio_parts裡音檔，只上傳"一個"**
![Imgur](https://i.imgur.com/TwbImgU.png)

#### **4.輸入指定prompt，跟音檔一起Run**

![Imgur](https://i.imgur.com/m1gigsx.png)


●prompt如下：
```txt
你是一位頂級的 AI 語音轉文字專家，專精於生成和格式化完全符合行業標準的 SRT 字幕檔案。你的輸出必須精確無誤。

SRT 結構的關鍵規則（必須毫無例外地嚴格遵守）：

序列號：一個從 1 開始並嚴格遞增的整數。

時間碼：  
格式絕對必須為 hh:mm:ss,xxx (小時:分鐘:秒,毫秒)。這是不可協商的。  
小時部分 (hh) 即使為零，也必須顯示為 00。例如，1 分 5 秒 9 毫秒應表示為 00:01:05,009，絕不能省略小時部分而寫成 01:05,009。此規則適用於檔案中的每一個時間碼。  
分鐘 (mm) 和秒 (ss) 若不足兩位數，必須以 0 在前面補齊（例如 00:01:05,009）。  
毫秒 (xxx) 必須為三位數，若不足三位數，必須以 0 在尾部補齊（例如 00:00:01,050 而不是 00:00:01,50）。  
開始時間和結束時間之間必須使用 --> (一個空格，兩個減號，一個大於號，一個空格) 分隔。  
時間碼行本身前後不得有任何多餘空格或字元。

字幕文字：  
核心原則：在每一個字幕塊中，此字幕文字內容必須且只能顯示為單獨的一行。嚴禁在單個字幕塊的字幕文字部分內部產生換行符或顯示為多行。

遵循下述「字幕生成規則」。  
空行：每個字幕塊 (包含序列號、時間碼、字幕文字) 之後，必須有一個且只有一個完整的空行 將其與下一個字幕塊分隔開。這是SRT格式的基礎。  
換行符：序列號行、時間碼行、以及字幕文字行，這三者各自作為獨立的行，它們之間必須使用標準換行符分隔。

字幕生成規則（請按優先級順序執行）：

第一優先：單行顯示與長度限制  
重申核心原則：每一字幕塊的字幕文字部分，必須且只能是一行。  
為確保此單行字幕易于閱讀，其文字長度絕對不能超過 15 個繁體中文字元。  
如果原始口語語句的自然長度超過 15 個字元，或者其語義停頓點暗示需要分行，則該原始語句必須被切分為 數個新的、獨立的字幕塊。每一個新切分出的字幕塊都將擁有全新的序列號和對應的時間碼，並且其自身的字幕文字部分嚴格遵守單行和 15 字元內的長度限制。

第二優先：語意分段與新字幕塊的創建  
當因上述「單行顯示與長度限制」原則需要切分原始口語語句時，切分點應選擇在最自然的語意停頓處（例如，在一個短語或子句結束後）。  
每一次有效的切分都意味著結束當前字幕塊，並為切分後的下一段文字創建一個全新的字幕塊。 這樣，原本可能導致在同一字幕塊內換行的內容，會被合理分配到連續的多個單行字幕塊中。

第三優先：時間長度  
每一段字幕（即每一個單行字幕塊）顯示的目標時長應在 3 到 5 秒 之間。  
請根據實際的語速和語氣停頓來微調，確保字幕與聲音同步。  
如果為了滿足單行和 15 字長度限制而切分出的字幕塊文字非常短，其顯示時間可以略短於 3 秒（例如 1-2 秒），但應盡量避免過於頻繁的極短字幕。

第四優先：內容淨化與精簡  
自動省略沒有意義的語助詞（如：嗯、啊、呃）、口吃或不影響語意的重複詞語（如：那個、那個）。  
字幕行中不包含任何標點符號（如：，。？！）。

最終指令：  
請根據提供的音檔，直接生成一份完全符合上述所有 SRT 結構和字幕生成規則的繁體中文字幕內容。再次強調，SRT 格式的精確性至關重要，特別是 確保每個時間碼都包含 hh: 部分 (即使是 00:)、每個字幕塊的字幕文字部分只有一行、時間碼的逗號、毫秒補零以及字幕塊之間的空行。最後輸出為 srt 檔案下載。"
```

#### **5.確認生成的srt是否符合格式以及是否有翻譯成繁體中文**

若沒有翻成繁體中文，再下一次如下prompt：
```txt
請翻譯成繁體中文，不要漏翻，並且修正字幕時間碼格式，符合SRT格式標準
```

若僅srt不符合格式，再下一次如下prompt：
```txt
請修正字幕時間碼格式，符合SRT格式標準
```

#### **6.字幕檔達標準就可以下載下來，副檔名直接用.srt儲存，小錯誤字幕軟體能自動修正**
![Imgur](https://i.imgur.com/ehpgNx0.png)

建議下載下來的Srt都經過字幕軟體自動修正

##### ●ai常見錯誤1:
`第一行 00:01.123 00.01.999`
→無小時→可以手動修正，一般第一行補上"00:00:01.123 00:00.01.999"字幕軟體能自己修

 這種錯誤，直接開啟字幕軟體，按儲存，就會修正了
![Imgur](https://i.imgur.com/mOJpbYN.png)


![Imgur](https://i.imgur.com/L7aFqdO.png)

##### ●ai常見錯誤2:
`第一行 00:01:123 00.01:999`
→毫秒前方錯誤使用分號
→下prompt讓ai修

```txt
請修正字幕時間碼格式，符合SRT格式標準
```

![Imgur](https://i.imgur.com/icWT6rL.png)


→若是還是不行，就改這個prompt:
```txt
請修正字幕時間碼格式，符合SRT格式標準

SRT 結構的關鍵規則（必須毫無例外地嚴格遵守）：

序列號：一個從 1 開始並嚴格遞增的整數。

時間碼：  
格式絕對必須為 hh:mm:ss,xxx (小時:分鐘:秒,毫秒)。這是不可協商的。  
小時部分 (hh) 即使為零，也必須顯示為 00。例如，1 分 5 秒 9 毫秒應表示為 00:01:05,009，絕不能省略小時部分而寫成 01:05,009。此規則適用於檔案中的每一個時間碼。  
分鐘 (mm) 和秒 (ss) 若不足兩位數，必須以 0 在前面補齊（例如 00:01:05,009）。  
毫秒 (xxx) 必須為三位數，若不足三位數，必須以 0 在尾部補齊（例如 00:00:01,050 而不是 00:00:01,50）。  
開始時間和結束時間之間必須使用 --> (一個空格，兩個減號，一個大於號，一個空格) 分隔。  
時間碼行本身前後不得有任何多餘空格或字元。
```

##### ●ai常見錯誤3:
`10分鐘影片出現srt時間不正常，未到9分多鐘`
→重跑：請重新整理頁面，重新上傳音檔、下prompt重跑


**重複步驟直到所有音檔跑完**

記住! 每次只上傳一個檔案，srt ok後要重整(清除記錄)→曾試過繼續丟檔案上去，時間軸會亂掉

![Imgur](https://i.imgur.com/QzmgmuQ.png)

### (3) srt檔加入開頭、末端標記，使未來合併字幕好自動對齊時間軸

<span style="background:#fff88f">首先，先將之前ai給的並處理好格式的srt複製一份放到別的資料夾備份</span>(以防萬一)


`可以直接使用我提供的"add_mark.bat"`

將這個bat放到與srt同一資料夾，雙擊後他會將這個資料夾裡的所有srt都插入開頭、末端時間標記
![Imgur](https://i.imgur.com/8PuRVDw.png)

處理完成的畫面

![Imgur](https://i.imgur.com/I3C71MC.png)

##### **--有興趣也可以照以下步驟自己建立--**

add_mark.bat
```bat
@echo off
chcp 65001 >nul
setlocal disableDelayedExpansion

set "current_dir=%~dp0"
pushd "%current_dir%"

for %%f in (*.srt) do (
    call :process "%%f" "%%~nf"
)

popd
echo.
echo ✅ 全部處理完成！
pause
exit /b


:process
setlocal
set "file=%~1"
set "name=%~2"

echo 處理檔案：%file%

(
    echo 0
    echo 00:00:00,000 --^> 00:00:00,001
    echo [SEGMENT START: %name%.mp3]
    echo(
    type "%file%"
    echo(
    echo 99999
    echo 00:09:59,000 --^> 00:09:59,001
    echo [SEGMENT END: %name%.mp3]
) > "temp_%~nx1"

move /Y "temp_%~nx1" "%file%" >nul

endlocal
exit /b

```

--步驟3結束--


### (4)合併字幕並對齊時間軸
合併之前請一再確認srt時間軸有沒有格式不對

`可以直接使用我提供的"merged.py"`

將這個 merged.py放到已標記srt同個資料夾後，雙擊merged.py，跑完會自動生成merged.srt在資料夾裡
![Imgur](https://i.imgur.com/pSDLtLu.png)


完成了!!! 此時也可以再用字幕軟體快速檢查一下
![Imgur](https://i.imgur.com/bsh1WgJ.png)


不用在意開頭與結尾標記，因為停留時間很短幾乎肉眼看不到
##### **--有興趣也可以照以下步驟自己建立--**
創立py檔，我都直接用notepad++：開新文件，複製下面code貼上，儲存檔案時副檔名選 .py

![Imgur](https://i.imgur.com/Q7MukJn.png)


![Imgur](https://i.imgur.com/OjNuJDA.png)


merged.py
```python
import srt
from pathlib import Path
from datetime import timedelta

def merge_srt_with_fixed_offset(segment_seconds=600):
    folder = Path(".")
    srt_files = sorted(folder.glob("*.srt"))
    all_subs = []

    for idx, srt_file in enumerate(srt_files):
        text = srt_file.read_text(encoding="utf-8")
        subs = list(srt.parse(text))
        current_offset = timedelta(seconds=segment_seconds * idx)
        for sub in subs:
            sub.start += current_offset
            sub.end += current_offset
            all_subs.append(sub)
    
    # 重新編號
    for i, sub in enumerate(all_subs, start=1):
        sub.index = i
    
    merged_content = srt.compose(all_subs)
    output_path = folder / "merged.srt"
    output_path.write_text(merged_content, encoding="utf-8")
    print(f"合併完成，輸出檔案：{output_path}")

if __name__ == "__main__":
    merge_srt_with_fixed_offset()

```

