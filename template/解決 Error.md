# 解決 Error
###### tags:`Python(語言)` `Compile Error(錯誤類型)` `cmd(其他關鍵字)` `venu(其他關鍵字)` `虛擬環境(其他關鍵字)`

## 錯誤描述:
在cmd中啟動檔案，輸入`something script`後，出現以下錯誤:
> Error code: description

## 原因: 

 - 這通常發生在「非原開發機」上，你在A機寫完py，移到B機就會出錯。

 - 因為你在原開發機上之所以能跑，是因為你已經在它的系統裡裝好了package。但是移動時這些package可沒跟著移。

而我這次是在A機上用PyCharm建立專案並在B機上執行，而PyCharm通常會幫你建好venu來執行專案。就是遇到該原因，也好好的認識了venu (virtualenv)。

## 認識與注意: 

 - 系統中的package跟venu中的package及功能是不相通的，包含pip、wheel、virtualenv(venu)、bs4...等。

 - 你裝好python並設置好系統變數後，pip install預設會裝在系統，除非你進入venu的pip所在資料夾。

## 解決: 

1. 首先查看你當前安裝的Eclipse的版本。在Eclipse功能表列中選擇"Help --> About Eclipse"，彈出一個對話方塊: 

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/template/1.png)

 > 圖9  查看Eclipse版本

2. 打開連結，向下滾動滑鼠，下載對應版本的語言包: 

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/template/2.png)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/template/3.png)

 > 圖10  對應版本的語言包

3. 重啟Eclipse，漢化完成，你可以享受中文版的Eclipse了。

## 如果還是不行:

1. 開啟Android Studio

2. 點擊Build>Clean Project

3. 點擊Build>Rebuild Project

4. 再將上面的步驟做一遍

## 參考: 

 - [[stackoverflow] ImportError: No Module Named bs4 (BeautifulSoup)](https://stackoverflow.com/questions/11783875/importerror-no-module-named-bs4-beautifulsoup)
 - [[csdn] python中虚拟环境的使用](https://blog.csdn.net/You_are_my_dream/article/details/53029233)