---
aliases: []
title:  pdf製作目錄-免費軟體FreePic2Pdf+PdgCntEditor
tags: [電子書or閱讀器, 程式]
categories:  電子書or閱讀器
date: 2023-02-17T17:14:19
modified: 2023-12-24T17:06:54
draft: false
toc: true
---
建立時間: 2023-02-17T17:14:19

標題: [ pdf製作目錄-免費軟體FreePic2Pdf+PdgCntEditor ]

tags: #電子書or閱讀器 #程式

---
# pdf製作目錄-免費軟體FreePic2Pdf+PdgCntEditor

---

>[!SUMMARY]+ Table of Contents
>- [pdf製作目錄-免費軟體FreePic2Pdf+PdgCntEditor](pdf製作目錄-免費軟體FreePic2Pdf+PdgCntEditor.md#pdf製作目錄-免費軟體FreePic2Pdf+PdgCntEditor)
>- [教學](pdf製作目錄-免費軟體FreePic2Pdf+PdgCntEditor.md#教學)
>    - [頁數偏移幾種方法](pdf製作目錄-免費軟體FreePic2Pdf+PdgCntEditor.md#頁數偏移幾種方法)
>    - [其他方式](pdf製作目錄-免費軟體FreePic2Pdf+PdgCntEditor.md#其他方式)

---
此篇發文於
1. https://www.facebook.com/groups/ereaderfamily/posts/6005226219534162/
2. 操作影片 https://youtu.be/U5u3gjk8pkw
3. 軟體下載點1 https://mega.nz/file/9BsVDS4a#Uriv4Coe324PYIzNrpyFlFdLwfspbJosFo9fyADViD8
4. 軟體下載點2 https://www.cnblogs.com/stronghorse/p/14967352.html

---
#軟體與小工具
本篇為秋雁大大紙本書數位化__第二篇裡製作目錄的衍生
秋雁大大文章: https://www.facebook.com/groups/ereaderfamily/permalink/4958918287498299/?mibextid=Nif5oz
**因為PDF-XChange Editor為付費軟體，所以另外提供免費軟體來替代。**

**作業系統**: win10
**軟體**: FreePic2Pdf、PdgCntEditor (原程式為簡體版，為了避免亂碼所以下載作者另外製作的英文版，以下也是用英文版教學)
**軟體下載點1**(我的彙整):https://mega.nz/file/9BsVDS4a#Uriv4Coe324PYIzNrpyFlFdLwfspbJosFo9fyADViD8
**軟體下載點2**(作者網站): https://www.cnblogs.com/stronghorse/p/14967352.html

------
# 教學
操作影片 https://youtu.be/U5u3gjk8pkw
1. **載點1** 下載FreePic2Pdf、PdgCntEditor並解壓縮，兩個放在同一資料夾裡。
2. 開啟FreePic2Pdf.exe
3. 右下角impt/expt點它
4. 頁籤選export
5. source pdf file開啟要轉的pdf檔
6. 按GO
7. 頁籤選import
8. The folder that interface file in:這條選第2個圖示
9. 輸出要修改成BIG5 儲存 (如果目錄為繁體中文的話一定要改!!!)
10. The folder that interface file in:這條選第3個圖示
11. 會跳轉到PdgCntEditor.exe
12. **直接** 【章節名頁碼】 貼上(**不須**如PDF-XChange Editor排版，也不須先分一二級目錄)，PdgCntEditor可以自動加頁碼(按上面圖示)，手動tab分級(按上面圖示) 
    →如果預先排版再貼入軟體不會理會，目錄分級要在PdgCntEditor裡加
13. 儲存
14. 注意要轉的PDF要關閉它!!
15. GO
成功!!回去原檔案那就是有添加目錄的pdf了
----
## 頁數偏移幾種方法
1. 在excel先處理頁數後再貼到PdgCntEditor
2. .PdgCntEditor上發有個+-符號可以輸入偏移量，例如第1章page1實際位在page9，就輸入+8

## 其他方式
其實我也有找到另一個開源軟體，不過還需要python運行(作者是python2.X我的是python3.X程式還要小改)，雖然會用但有點麻煩，有興趣研究的也可以看看  
https://github.com/syaoo/pdfbookmark

