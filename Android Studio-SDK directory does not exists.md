# Android Studio-SDK directory does not exists
###### tags:`Android Studio` `IDE`

## 錯誤描述:

複製Android Studio 工程到其它電腦後遇到:

> Error:A problem occurred configuring project ':app'.

> The SDK directory '/Users/alex/Library/Android/sdk' does not exist.

## 解決: 

在專案的根目錄下找到檔:  `local.properties `，打開並找到如下行

`sdk.dir=/Users/alex/Library/Android/sdk`

> 注意:Studio預設開啟的檔案並非根目錄的

改為新電腦Sdk所在的目錄，比如: 

`sdk.dir=/home/azhu/Android/Sdk`

> 注意:直接從檔案總管複製路徑時要注意正反斜線( \、/ )的差別

## 參考: 
  - [[csdn] 复制Android Studio 工程到其它电脑后遇到The SDK directory 'XXXX‘ does not exist.问题的解决方法](https://blog.csdn.net/dotphoenix/article/details/50378132)