# 把電子報轉成RSS訂閱
###### tags: `blog` `rss` `電子報`

## 參考
  - [把電子報轉成RSS訂閱](http://blog.pulipuli.info/2013/12/rss-forward-e-mail-newsletter-to-rss.html)
  - [[電腦玩物] Feedly 完全上手教學，延續 Google Reader 閱讀器體驗](http://www.playpcesor.com/2013/03/feedly-google-reader.html)

## 情境說明

我現在想要將Gmail中部分郵件自動轉寄到以Blogger建立的電子報Blog，利用Blogger的「使用電子郵件張貼」(Mail2Blogger)功能來張貼電子郵件。最後就用Feedly訂閱電子報Blog，完成訂閱的動作。

## 事前準備

 - [Google Account](https://accounts.google.com/ServiceLogin?service=blogger&passive=1209600&continue=http://www.blogger.com/home&followup=http://www.blogger.com/home&ltmpl=start): 使用Gmail、Blogger跟Feedly都會用到的帳戶。如果還沒有Google帳戶，[去免費註冊一個吧](https://accounts.google.com/SignUp?service=blogger&continue=http%3A%2F%2Fwww.blogger.com%2Fhome&ltmpl=start)。

 - [Gmail](https://mail.google.com/mail/): 接收電子報的電子郵件地址，並且進行自動轉寄的功能。你也可以用你自己偏好的電子郵件系統，大部分也都有提供轉寄的功能。

 - [Blogger](http://www.blogger.com/?hl=zh-TW&tab=jj): 保存電子報，並提供RSS訂閱的免費服務。

 - [Feedly](http://feedly.com/): 訂閱RSS的閱讀器。我會搭配gReader來讀取在Feedly訂閱的RSS，不過gReader在本教學中不是重點。

準備好的話，請按照以下步驟，一步一步把電子報轉換成RSS訂閱吧。

## 步驟
### 建立電子報Blog
進入[Blogger的首頁](http://www.blogger.com/home?pli=1)，點入左上角的「新增網誌」按鈕。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/1.png)

輸入標題與網址就可以建立了。在此我輸入的是「布丁測試電子報」 (以下簡稱電子報Blog)與「pulipuli-test-newsletter.blogspot.com」。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/2.png)

進入新建立電子報Blog的「設定」功能，進行一下的其他設定。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/3.png)

### 關閉隱私權
在「設定」的「基本」中，將隱私權關閉，因為這只是我私人使用的電子報訂閱位置。如果你不介意公開訂閱的電子報，那也可以把它打開。
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/4.png)

### 關閉留言
在「設定」的「文章和留言」中，把留言功能限定於「僅限此網誌的成員」，再按右上角的「儲存設定」。因為這只是我私人使用的電子報，不希望讓別人留言討論。
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/5.png)

### S設定使用電子郵件張貼功能
這一步重要！進入「行動裝置及電子郵件」中，設定「使用電子郵件張貼」的功能。文字框裡面你可以輸入指定的密語(secret words)，組成一個只有你知道的電子郵件位置，再按下右上角的「儲存設定」。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/6.png)

舉例來說，我設定的是「test-newsletter」，於是未來任何人寄信到到「pulipuli.chen.test-newsletter@blogger.com」時，他都會直接發佈在Blog當中。當然，這個位置我只是測試用的而已，寫完這篇文章之後我就會刪除了，請不要真的去寄信。

### 關閉「關於我自己」的訊息

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/7.png)

Blogger預設會在Blog擺放自己的資訊。因為這只是電子報保存，不代表我個人的文章，所以建議把它移除掉。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/8.png)

你可以從「版面配置」中找到「關於我自己」，按下「編輯」後再選擇「移除」按鈕，就可以關閉這個訊息。

#### Gmail新增轉寄位置
為了把[Gmail](https://mail.google.com/)轉寄到電子報Blog，必須先在Gmail的設定中新增「轉寄地址」。在Gmaill「設定」的「轉寄和POP/IMAP」中進入「新增轉寄地址」。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/9.png)

在此輸入剛剛在電子報Blog新增的電子郵件張貼位置「pulipuli.chen.test-newsletter@blogger.com」，按下一步。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/10.png)

確認郵件轉寄，按下「繼續」。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/11.png)

回到電子報Blog的首頁上，你會發現有一篇文章被新增了，而且還是Gmail的轉寄確認信。點下信中提供的連接已確認郵件吧。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/12.png)

確認成功。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/13.png)

接著再回到電子報Blog的管理介面中，刪除剛剛那篇「Gmail轉寄確認」的文章吧。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/14.png)

### Gmail建立電子報篩選器，自動轉寄到Blog
在Gmail中，利用篩選器來選擇電子報的寄信來源。
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/15.png)

以「圖書館」的電子報為例，我可以用寄件者為「fish14@nccu.edu.tw」這位館員的電子信箱作為篩選條件，按「根據這個搜尋條件建立篩選器」來建立篩選器。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/16.png)

接著我再篩選器中設定「轉寄給: pulipuli.chen.test-newsletter@blogger.com」跟「刪除它」，以及勾選「略過收件匣(將其封存)」、「永不將其標示為重要」跟「分類為: 最新快訊」。以此設定按下「建立篩選器」。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/17.png)

好，到目前為止，我們總算可以把Gmail的電子報轉移到電子報Blog中了。

### 用Feedly訂閱電子報Blog的RSS
電子報Blog的RSS訂閱位置，預設是在網頁下方的「訂閱:文章 (Atom)」中。以電子報Blog為例，它的網址是「http://pulipuli-test-newsletter.blogspot.tw」，那RSS訂閱位置就是「http://pulipuli-test-newsletter.blogspot.com/feeds/posts/default」。記住這個訂閱位置，Feedly就是靠這個位置來訂閱RSS的。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/18.png)

接著我們來到Feedly頁面，從「+Add Content」功能中，在搜尋框輸入剛剛的RSS訂閱位置。等一段時間後，Feedly會找到該RSS訂閱的來源(Discover feeds)，再按下「+」新增。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/把電子報轉成RSS訂閱/19.png)

這樣子就完成在Feedly中訂閱RSS的動作了。至於要怎麼在Feedly整理RSS訂閱或其他的功能，就請參考[電腦玩物寫的「Feedly 完全上手教學，延續 Google Reader 閱讀器體驗」](http://www.playpcesor.com/2013/03/feedly-google-reader.html)吧。