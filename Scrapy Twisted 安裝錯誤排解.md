# Scrapy Twisted 安裝錯誤排解
###### tags:`Python` `Compile Error` `windows` `Scrapy`

### 錯誤描述
使用PyCharm執行scrapy出現以下錯誤

> 無法下載，點開來是microsoft visual C++ 14.0建構錯誤

## 原因: 
可用pip指令安裝Twisted來繞過錯誤

### 解決方法

 - 確認安裝wheels並更新至最新: 

`pip install wheel --upgrade`

 - 下載相符python版本的[Twisted](https://www.lfd.uci.edu/~gohlke/pythonlibs/#twisted)，這裡很特別，雖然我是x64電腦卻只能跑x32，可能是我當初安裝錯誤

 - 下載好後，輸入cmd指令，安裝Twisted

`pip install C:\User\Twisted-17.9.0-cp36-cp36m-win_amd64.whl`

 - 完成

### 注意
x32跟x64容易搞混，請再三確認版本

### 參考
 - [[Stack Overflow] Installing twisted on python 3.5 and virtualenv using pip](https://stackoverflow.com/questions/42285617/installing-twisted-on-python-3-5-and-virtualenv-using-pip)
 - [[stackoverflow] python 3.x - Twisted-17.9.0-cp27-cp27m-none-win_amd64.whl is not a supported wheel on this pl](https://stackoverflow.com/questions/49568976/twisted-17-9-0-cp27-cp27m-none-win-amd64-whl-is-not-a-supported-wheel-on-this-pl)

 - [[csdn]Python3环境安装scrapy库发生的问题解决方法](https://blog.csdn.net/create115721/article/details/79238696)
 - [[kknews] Python爬蟲之不要入了Scrapy安裝的「坑」](https://kknews.cc/zh-tw/finance/lzmk5b9.html)
