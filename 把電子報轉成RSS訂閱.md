# 把電子報轉成RSS訂閱
###### tags: `架站` `rss` `blog`
 參考至:[http://blog.pulipuli.info/2013/12/rss-forward-e-mail-newsletter-to-rss.html](http://blog.pulipuli.info/2013/12/rss-forward-e-mail-newsletter-to-rss.html)

#### 情境說明與事前準備 / Preparing

我現在想要將Gmail中部分郵件自動轉寄到以Blogger建立的電子報Blog，利用Blogger的「使用電子郵件張貼」(Mail2Blogger)功能來張貼電子郵件。最後就用Feedly訂閱電子報Blog，完成訂閱的動作。

因此在以下教學中，我會用到幾個工具：

*   [Google Account](https://accounts.google.com/ServiceLogin?service=blogger&passive=1209600&continue=http://www.blogger.com/home&followup=http://www.blogger.com/home&ltmpl=start)：使用Gmail、Blogger跟Feedly都會用到的帳戶。如果還沒有Google帳戶，[去免費註冊一個吧](https://accounts.google.com/SignUp?service=blogger&continue=http%3A%2F%2Fwww.blogger.com%2Fhome&ltmpl=start)。

*   [Gmail](https://mail.google.com/mail/)：接收電子報的電子郵件地址，並且進行自動轉寄的功能。你也可以用你自己偏好的電子郵件系統，大部分也都有提供轉寄的功能。

*   [Blogger](http://www.blogger.com/?hl=zh-TW&tab=jj)：保存電子報，並提供RSS訂閱的免費服務。

*   [Feedly](http://feedly.com/)：訂閱RSS的閱讀器。我會搭配gReader來讀取在Feedly訂閱的RSS，不過gReader在本教學中不是重點。

準備好的話，請按照以下步驟，一步一步把電子報轉換成RSS訂閱吧。

#### Step.1 建立電子報Blog / Create Newsletter Blog

![image](https://lh3.googleusercontent.com/6rmIvyD9JWcUKJQFUOoFNGm1LOaTgZWshMiZYWplp5sz-bdcdVgyJqLa4GI5Po6BX3CnyqlRB-5351t2vVXM7X84XR_kyGnhYB6zOywtfLgfnPh_WNp3bWq5AweS_cz2RuYyTPKp "image")

進入[Blogger的首頁](http://www.blogger.com/home?pli=1)，點入左上角的「新增網誌」按鈕。

![image](https://lh4.googleusercontent.com/ihz-ThlAosG-XdX95XmHzZyeitOG2ekrCeZ-bHQSBjJbhBk0iU-uN81pjkLZNRtnBmEtZvFbCSkazLuf0hD4zh7R_OtVsNNihHtwCogPc1xXSnG5LXmsjFnEIupXlP6AVOOI3ixH "image")

輸入標題與網址就可以建立了。在此我輸入的是「布丁測試電子報」（以下簡稱電子報Blog）與「pulipuli-test-newsletter.blogspot.com」。

![image](https://lh5.googleusercontent.com/ngbXAa4Sbc_aQhgfJVOOD00vlHe6rELCsnuERJwcDpNap9emzDI3yJCcRi6R5qcqXTD-ompFaWjWAdetFAPfa1PYNcVhndBBVi0HyjkiGH2Cf8EQp6gldcWf30NEhUfTZGNBYD_Z "image")

進入新建立電子報Blog的「設定」功能，進行一下的其他設定。

#### Step 1-1\. 關閉隱私權 / Setup Private

![image](https://lh4.googleusercontent.com/ccNuKN60EK1MzyHnp40T-GdwMKPcnKV4IMYiUHoBjHjRZ7m_JmSwe7XOtxjvdzNDVNHhLcjg3QxxBGt7sLfVTdQ7GqDA8kipGh5jAWd2cAvB-V1T2PhPXA8Dp_olUvvkyIl10sYz "image")

在「設定」的「基本」中，將隱私權關閉，因為這只是我私人使用的電子報訂閱位置。如果你不介意公開訂閱的電子報，那也可以把它打開。

#### Step 1-2\. 關閉留言 / Disable Comment

![image](https://lh5.googleusercontent.com/2MlRr1tpi2fgNmWiIGwi_Q2RycqL9kVIjGZ19hJWL1y7gYjpjU3mtKkNF56A3DY5VLk-YVfAh05vXhHmxBQvbpcthSTvM5m5j77Gv4yZO-lawvCAlgNhjLIK6f-7emlW690QQv8w "image")

在「設定」的「文章和留言」中，把留言功能限定於「僅限此網誌的成員」，再按右上角的「儲存設定」。因為這只是我私人使用的電子報，不希望讓別人留言討論。

#### Step 1-3\. 設定使用電子郵件張貼功能 / Enable Mail2Blogger

![image](https://lh4.googleusercontent.com/ErmGvRXCH1oJabZ7-xIc_WbFhu79nciQJIpKLfIKISbkcn5VGgmF9znPSNmm56BpYNC6JAVug7RbT_FwNdQbdU13ExgUuK-AW_ScKh1MvD63z3c1miUZ6cC4VDvIX_HjGNuiE2I4 "image")

這一步重要！進入「行動裝置及電子郵件」中，設定「使用電子郵件張貼」的功能。文字框裡面你可以輸入指定的密語(secret words)，組成一個只有你知道的電子郵件位置，再按下右上角的「儲存設定」。

舉例來說，我設定的是「test-newsletter」，於是未來任何人寄信到到「pulipuli.chen.test-newsletter@blogger.com」時，他都會直接發佈在Blog當中。當然，這個位置我只是測試用的而已，寫完這篇文章之後我就會刪除了，請不要真的去寄信。

#### Step 1-4\. 關閉「關於我自己」的訊息 / Hide Author Information

![image](https://lh4.googleusercontent.com/5ydoDdeTLQtFPxB6qOekVOqlmwBk8UIc0TZiWhdTJLt7Ko4TY8peJRqYSrbikxOLP8g5H5mBYPWEYLk8Wfd0H11WY83SUdhRK-8IUGzQ6ux8xgeX6aZYSU7ngNWDHKJKwVR60gWG "image")

Blogger預設會在Blog擺放自己的資訊。因為這只是電子報保存，不代表我個人的文章，所以建議把它移除掉。

![image](https://lh6.googleusercontent.com/kSlS_2V-qOxDAPJj9NVJYINezQxrLz9YLOy0__uFNxxhYnsb_of_9tUKXfYXCZbC3aJB7aij2sf14cc0G7VyuzqwqPcTL5pa5YrqJ7lwxPoB0YyDBFg1S1WItM4-JneqKiqHXnQA "image")

你可以從「版面配置」中找到「關於我自己」，按下「編輯」後再選擇「移除」按鈕，就可以關閉這個訊息。

#### Step 2\. Gmail新增轉寄位置 / Setup Forward in Gmail

![image](https://lh6.googleusercontent.com/GSqgkpbDlzUIwpzmuV2zntLkJeKiMVQBxQVvtQJaDnEArzaAxEUd12NI_VngoM4t0CUd2AkaoIn9xYveWnj61rYjLbCN32bEuEzo_foMi1FiVkp6oByAxVWU_Hc9MabpAXXC1WhO "image")

為了把[Gmail](https://mail.google.com/)轉寄到電子報Blog，必須先在Gmail的設定中新增「轉寄地址」。在Gmaill「設定」的「轉寄和POP/IMAP」中進入「新增轉寄地址」。

![image](https://lh6.googleusercontent.com/GNiEbhJho28pVbYCWOta276xAvhaNO0FmMKlkkYj8yYs9Agm_0JRFgUj1aPqGmN9M7pFDFXjLrEFJBvTSYCUP7D112mPj13d-65NSpRkXQDhsV3YycZpJF7kD8R_ECr1bHHhD54k "image")

在此輸入剛剛在電子報Blog新增的電子郵件張貼位置「pulipuli.chen.test-newsletter@blogger.com」，按下一步。

![image](https://lh6.googleusercontent.com/Cxc12dEGxpvbD14wBT3ZOminfYzn8YeVw8zmGLYHK6TtrRfEbZG5abNoNC-fj7vITQR8s5y_m0k4exi80w9TAcNe1nX99tUIzObJEnOcX4weFZFQOhBGmKi5ScoWM7oXLu-NZ5ML "image")

確認郵件轉寄，按下「繼續」。

![image](https://lh5.googleusercontent.com/p_i_INmTdQKeJ1TX8LAbeUOsxHhj0ZROfAejmTqvc1Bvl3QOamj7JQP8OLCWHKdXbYft0OCo9q85B3aMfKW61HE2YLoez2u_hSd5Pjg1RkngGNVDuo6di3Y-aiHXtGdU8BsaQ1wK "image")

回到電子報Blog的首頁上，你會發現有一篇文章被新增了，而且還是Gmail的轉寄確認信。點下信中提供的連接已確認郵件吧。

![image](https://lh4.googleusercontent.com/rXPpKuvP5mR-roKMDp27UMmcmaazULurXslndMfJmPURcjlWsD_dMvHQjZoWdlGkOcelNe_LRyns02_JlxVt163Rj60GoVbFx3JRhxxHMZ-RIWMj0Fx8UiTgLxAveog0lfqM2czO "image")

確認成功。

![image](https://lh5.googleusercontent.com/Rkptdo2WvjV-pBwog3vtEqVzlW8dyWc1ktUnJ2ucVOrtluWUh-6tiF9WNIZ-AuzePgUpAhTZ32QenLd1G-qPibSksedoUykr59nOBTMZUsUbD4BHyizzOQuEJvAwhNovo4VEvD-r "image")

接著再回到電子報Blog的管理介面中，刪除剛剛那篇「Gmail轉寄確認」的文章吧。

#### Step 3\. Gmail建立電子報篩選器，自動轉寄到Blog / Use Gmail Filter to Forward Newsletter to Blog

![image](https://lh6.googleusercontent.com/PH2GBl03j1Q_z1k37Z2s_a5fCdoqn-irpIk8QtjrvFgj4jXJV8h7q6CUjY14dLMVizuBT1qicAiutCf_h7_rQ4mtyfRnrxObjKSAp_QLohR2_Gkml5ZFjhRxAg7NvBEDcbwB9dxG "image")

在Gmail中，利用篩選器來選擇電子報的寄信來源。

![image](https://lh3.googleusercontent.com/reKJ6E-BcUn4PoDkZ1DoYg6vfcp1RGWvJO07U1HBdxqK4GMXEzJuthsTeG6YfpSOVlUvc_Jj6SmsAE9_eZD85_u3YaD9Nz7A1Rpri3lK1bmfrwqx7yRPWsOZP6VJVKJxYQwZKgFS "image")

以「圖書館」的電子報為例，我可以用寄件者為「fish14@nccu.edu.tw」這位館員的電子信箱作為篩選條件，按「根據這個搜尋條件建立篩選器」來建立篩選器。

![image](https://lh5.googleusercontent.com/uh1wjlcIR_AIFgupq091-rok7oBQ3FmSOSb6iAC1yOhUgCSx_g-PCBc2fT3UrhMz3A79_5hugVtfz2k8jP6BwPOFPHyLvLlLvrUMWFm-UdI48ZndZaOhVxegk9J-od_FOgH67doe "image")

接著我再篩選器中設定「轉寄給：pulipuli.chen.test-newsletter@blogger.com」跟「刪除它」，以及勾選「略過收件匣(將其封存)」、「永不將其標示為重要」跟「分類為：最新快訊」。以此設定按下「建立篩選器」。

好，到目前為止，我們總算可以把Gmail的電子報轉移到電子報Blog中了。

#### Step 4\. 用Feedly訂閱電子報Blog的RSS / Subscribe RSS feed in Feedly

![image](https://lh5.googleusercontent.com/ZHpaUGvv89Ir-XUaf-OcA71VMZ4JD-K8RrAGx8xKWelYofhqZCY1LGPnV_RlAyywSsjK-gIIK5AXXhopfsaZL3bTUdoEeQ7XpeqzrEIxG60uOFEkrS78Msx7WvUdzXihijhnFRIy "image")

電子報Blog的RSS訂閱位置，預設是在網頁下方的「訂閱： [文章 (Atom)](http://pulipuli-test-newsletter.blogspot.com/feeds/posts/default)」中。以電子報Blog為例，它的網址是「[http://pulipuli-test-newsletter.blogspot.tw/](http://pulipuli-test-newsletter.blogspot.tw/)」，那RSS訂閱位置就是「[http://pulipuli-test-newsletter.blogspot.com/feeds/posts/default](http://pulipuli-test-newsletter.blogspot.com/feeds/posts/default)」。記住這個訂閱位置，Feedly就是靠這個位置來訂閱RSS的。

![image](https://lh5.googleusercontent.com/DG6YgLnoILVv0yb2xZI3p-r8yI7U3mqkWfY6nfKCE-app6RfDAaeN57-bAKeUaFC9pJo-hEZU2PMpiONNOOH0Ci7I2OZEfXF5NlanjR-x2H82j3SNr30lvPeOaTrN9OvPMBL5taH "image")

接著我們來到Feedly頁面，從「+Add Content」功能中，在搜尋框輸入剛剛的RSS訂閱位置。等一段時間後，Feedly會找到該RSS訂閱的來源(Discover feeds)，再按下「+」新增。

這樣子就完成在Feedly中訂閱RSS的動作了。至於要怎麼在Feedly整理RSS訂閱或其他的功能，就請參考[電腦玩物寫的「Feedly 完全上手教學，延續 Google Reader 閱讀器體驗」](http://www.playpcesor.com/2013/03/feedly-google-reader.html)吧。