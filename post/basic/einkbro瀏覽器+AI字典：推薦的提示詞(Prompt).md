---
aliases: 
title: einkbro瀏覽器+AI字典：推薦的提示詞(Prompt)
tags:
  - 電子書or閱讀器
categories: 電子書or閱讀器
date: 2024-08-11T21:58:47
modified: 2024-08-13T18:25:41
draft: false
toc: true
---

建立時間: 2024-08-11T21:58:47

最後修改日: 2024-08-11T21:58:47

tags:  #電子書or閱讀器

---
# einkbro瀏覽器+AI字典：推薦的提示詞(Prompt)

```toc
```
**<font color="#ff0000">來源：</font>
1. FB發文處 https://www.facebook.com/groups/ereaderfamily/posts/8143143705742392/
2. 
3. 
---
# einkbro瀏覽器+AI字典：推薦的提示詞(Prompt)
#einkbro #AI #chatgpt #字典

在開放式閱讀器，如果想使用**AI**(例如chatgpt)當作**字典**來**解釋詞語、翻譯或單字學習**，可以使用einkbro瀏覽器代勞。
除了在einkbro瀏覽器中直接使用AI解釋功能外，某些閱讀app(例如boox閱讀器裡的neoreader、靜讀天下app)也支援第三方應用程式字典，因此你可以指定einkbro作為字典。

而AI使用關鍵的一環為**提示詞(Prompt)**。

**以下內容分為幾部分**：1.首先講解提示詞的修改歷程，未來你想修改時有個方向。2.接著分享幾個我try出來覺得不錯的提示詞。3. 然後介紹如何申請API key以及其它應用。最後講4.如何在boox閱讀器和靜讀天下App中設定einkbro為字典。

**我的提示詞只是嘗試後覺得不錯的組合，不一定最好，歡迎大家分享自己的提示詞。特別感謝Daniel Kao大大為einkbro瀏覽器附加AI跟字典調用功能。**

**會使用兩大AI：openai (chatgpt)跟gemini  (google AI)**
einkbro為 V11.13.0(08100027)版

**OpenAI的回覆風格更合我意**，但感覺沒有新資料訓練，所以對於**較新事物我會使用Gemini**。OpenAI一開始會送你試用，到期後需先儲值(最低儲值金額5美金)付費使用(我有儲值，反正很萬用我還有用在別的地方，而且花費非常低)。Gemini AI目前有一定免費額度，如果不想花錢，可以使用它，但短時間高頻率問它會卡住。

不想看誕生過程的直接跳"**推薦的提示詞**"那段

# 一、提示詞的誕生
我參考了OpenAI Translator的回覆格式、Pubook Pro的ChatGPT回覆照片，以及Sider ChatGPT側邊欄的提示詞，並根據這些設計我的提示詞，你也可以參考各家AI應用程式，並思考你希望AI回覆的內容。例如：
我參考OpenAI Translator回覆格式，讓AI在輸入某個外文單詞時回覆各個時態、詞性、例句及字根來源。附帶一提，你可以指定AI的回答模板，避免AI隨意發揮。

版上有人po pubook pro的問chatgpt回覆照片，看到後想到可以做一個通用提示詞，不僅能翻譯成中文，還能解釋詞義，並列出單詞的多個意思。所以我做了一個通用版，以及一個通用版+單字學習版。

突然想到，有時看文遇到網路流行語，但我還跟上最新流行未知其意時，發現OpenAI不能正確回覆，只好改用會連網的gemini AI。

中間經過好多次修改，例如，AI有時會將我的問題當作稱讚它(笑)，像是未修改完的提示詞曾經測試時問他"獲益良多"，要它解釋詞意，AI竟回覆我"謝謝" XDDD

![Imgur](https://i.imgur.com/fm8UXV8.png)

![Imgur](https://i.imgur.com/XTEh33O.png)

![Imgur](https://i.imgur.com/JdrpD45.png)

# 二、推薦的提示詞
1. 通用版
   `等下給的"任何"詞或句子。請若為名詞、詞彙、成語、特殊用語、動詞、狀態詞、褒貶詞等等請詞語解釋。非中文語言則全文翻譯成繁體中文，若是單一詞語有多個意思就直接列出所有意思。以繁體中文回覆：`
   
2. 通用進階版
   `以繁體中文回覆，等下給的"任何"詞或句子。請若為名詞、詞彙、成語、特殊用語、動詞、狀態詞、褒貶詞等等請詞語解釋。非中文語言則全文翻譯成繁體中文，若是單一詞語有多個意思就直接列出所有意思且需包含單字、詞性、解釋與3個常用例句以及例句翻譯(提供原本語言與zh-tw對照)。`  
   
3. 解略回覆版
   `請用繁體中文，清楚、簡潔地解釋以下內容：`
   
4.  英文單字學習版
等下給的"任何"單詞或句子(此為[原句])，告訴我它的[語言]，例如美語。它是名詞、形容詞、動詞還是副詞等等(此為[詞性])。它的kk音標。翻譯成繁體中文後的意思有哪些(此為[翻譯])並解釋[原型](原本語言)，以及各種過去、過去進行、未來、未來進行、複數、單數等[型態]。以及詞源。與3個常用例句（跟輸入詞的語系相同，此為[例子]，並提供原本語言與zh-tw對照。)
並依照以下排列呈現:
[原句]/kk音標
[語言]/ [詞性]
[翻譯]
[原型]
[型態]
[例子]
[詞源]

5. 網路流行用語、時事梗、迷因版(例如i人、e人、山道猴)
   `等下"任何"內容請給出目前網路流行用語的解釋意思，用繁體中文回答:`
   →記得開啟"**use google gemini model**"
   →現在流行用語、時事梗、迷因更新換代太快，AI有時會亂回答喔
   
6. 日文學習版(對日文沒很熟，可能得要再修，漢字有時會誤以為是中文)
等下給的"任何"單詞或句子(此為[原句])是日語。它的詞性(此為[詞性])。它的羅馬拼音、漢字。翻譯成繁體中文後的意思有哪些(此為[翻譯])並解釋[原型](原本語言)以及詞源，以及各種名詞、形容詞、動詞、副詞型態(此為[型態])。與3個常用例句（跟輸入詞的語系相同，此為[例子]，並提供原本語言與zh-tw對照。)
並依照以下排列呈現:
[原句]/羅馬拼音
日語/ [詞性]/漢字
[翻譯]
[原型]
[型態]
[例子]
[詞源]

7. 其它語言就以此類推~
   

有時AI沒正確回答，可以多按幾次，但如果多次嘗試後仍無效，可能需要更換提示詞。
目前有幾個沒設置回答模板，可以根據需求自行製作。

**另外，因為我用字典頻率不高，所以model我用比較貴的gpt-4o；若想省錢可以選擇gpt-4o-mini或gpt-3.5-turbo ，價格差蠻多。gemini方面，我用1.5-pro，但若查詢頻率高我會換成1.5-flash。**


# 三、如何申請openai key(chatgpt)跟gemini key (google AI)
## openai key(chatgpt)
到openai網站(https://platform.openai.com/signup)註冊帳號後，點右上角**Dashboard**，再看左邊菜單有沒有出現"**API key**"→右上方點選「**Create new secret Key**」→命名後create→生成的一串英文數字就是key，請複製儲存(同一key可以用在多個程式上，所以請妥善保存，忘了就得再重新申請，也請不要洩漏給他人)。試用用完後要儲值(信用卡刷卡)才能繼續使用。
(網路上翻翻應該也能找到免費(或低價)key，為了省麻煩我直接官方付費)
![Imgur](https://i.imgur.com/s0Ec16t.png)

![Imgur](https://i.imgur.com/k2UaAoE.png)
![Imgur](https://i.imgur.com/vCg2JZd.png)

![Imgur](https://i.imgur.com/rPGsid8.png)

## gemini key (google AI)
到 Google AI Studio點Get API key (https://aistudio.google.com/app/apikey?hl=zh-cn)→創建API密鑰(create API key)→Create API key in new project→生成的一串英文數字就是key，請複製儲存(同一key可以用在多個程式上，所以請妥善保存，忘了就得再重新申請，也請不要洩漏給他人)。
![Imgur](https://i.imgur.com/AA4rNtp.png)

![Imgur](https://i.imgur.com/oZYlH3h.png)

![Imgur](https://i.imgur.com/Kl4jrIK.png)

![Imgur](https://i.imgur.com/bAGX6Cn.png)

## 其它應用
可以用在OpenAI Translator(解釋、總結、分析、改寫)、沉浸式翻譯(文章或書籍雙語翻譯)、文字轉語音製作有聲書、calibre某些可以雙語翻譯書籍的外掛


# 四、boox閱讀器裡的neoreader跟靜讀天下app怎麼設定einkbro當字典
## einkbro設定
下載einkbro後，到einkbro的設定**填"openai api key"跟"chatgpt功能列表(提示詞)"並開啟"use it on dict search"**，如果要用gemini則填下方"gemini api key"並勾選使用(use google geminin model)，不要用gemini就不勾。
**提示詞可以多設幾個**:在chatgpt功能列表
**model部分**：openai要好的回答就用貴一點的gpt-4o，省錢可以用gpt-4o-mini或gpt-3.5-turbo (如果不是很難的問題)。gemini可以用1.5-pro (比較好但免費額度少)，用完了改用1.5-flash，flash回答速度比較快但簡易。
![Imgur](https://i.imgur.com/LUlPiQM.png)

## boox neoreader
einkbro設定完後，neoreader圈選要翻譯的片段，選下方右邊數第3個像書本圖案的→選"einkbro"。提示詞可以依照需求多設置幾個

## 靜讀天下
點開一本書→右上角...→其它選項→自訂辭典→選"其它已安裝應用程式"→einkbro

# 情報
Daniel大大補充資訊：如果你在 prompt 中有使用 <<>> 的話， EinkBro 在把資訊帶給 OpenAI 時，會把前後文也加進去。所以，比方說我的 單字解釋 prompt 是這麼下的: be concise.

1. according to input below, use 繁體中文 to explain words in <<>>

2. original word form of content that is in <<>>

3. example in original language, and its translation in zh-tw

example:

Input: l <<ate>> a lot of snacks.

1. 吃，將食物從嘴放入，汲取營養

2. eat

3. I like to eat

(我愛吃)

here's the input:

![Imgur](https://i.imgur.com/6Ih9Hjy.png)



現在 gpt-4o-08-06 有再便宜一半的價錢，建議切換到 gpt-4o-08-06，可以用得更開心。而 gemini-1.5-flash 每分鐘可以免費呼叫 15 次；gemini-1.5-pro 則是每分鐘免費兩次。
