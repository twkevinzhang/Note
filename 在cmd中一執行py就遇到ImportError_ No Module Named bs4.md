# 在cmd中一執行py就遇到ImportError: No Module Named bs4
###### tags:`Python` `error` `cmd` `venu` `虛擬機`
這問題困擾了我兩天：當你裝好python3.x，在Windows的cmd中執行main.py時，出現：failed:no module named bs4

## 原因：

1.  這通常發生在「非原開發機」上，你在A機寫完py，移到B機就會出錯。

2.  因為你在原開發機上之所以能跑，是因為你已經在它的系統裡裝好了package。但是移動時這些package可沒跟著移。

3.  這個py是在venu中執行，而你在cmd中卻是要求用系統執行。venu中的package可不會跑到系統上去。所以你必須啟動venu來執行py。

而我這次是在A機上用PyCharm建立專案並在B機上執行，而PyCharm通常會幫你建好venu來執行專案。就是遇到該原因，也好好的認識了venu、virtualenv。

## 認識與注意：

1.  系統中的package跟venu中的package及功能是不相通的，包含pip、wheel、virtualenv(venu)、bs4...等。

2.  你裝好python並設置好系統變數後，pip install預設會裝在系統，除非你進入venu的pip所在資料夾。

3.  venu就是一種python的虛擬環境，類似java。你可以進入venv\Scripts中執行activate來啟動。

## 解決：

進入venu再執行py即可。

## 參考：

[https://stackoverflow.com/questions/11783875/importerror-no-module-named-bs4-beautifulsoup](https://stackoverflow.com/questions/11783875/importerror-no-module-named-bs4-beautifulsoup)

[https://blog.csdn.net/You_are_my_dream/article/details/53029233](https://blog.csdn.net/You_are_my_dream/article/details/53029233)