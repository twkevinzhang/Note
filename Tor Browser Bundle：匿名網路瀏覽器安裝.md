# Tor Browser Bundle：匿名網路瀏覽器安裝
###### tags:`瀏覽器` `tor` `暗網` `vpn`
 參考至:
  - https://blog.timshan.idv.tw/2014/01/how-to-tor-browser-bundletor.html

![](https://lh5.googleusercontent.com/Vun94fLYc_pSsP9qDByC1qlYQUpnDpx4HUK2indSNMbt_zEHmQX9XzAr1H7Qtq0m6ET-tlZ5NQGRUIK1zOWJ8ive0lRvEGoCuCZ8kAF2RmGJrQvJxRKRS1WveqYHO8MPA7Blkbb6hlNa2Ho_HA)

現在如果提到匿名網路，最廣為人知的大概就是洋蔥路由(The Onion Router)，當初美國海軍為了建立一個不被監聽的網路以保護政府通訊而贊助[Tor Project](https://www.torproject.org/)，其隱匿性之高連NSA內部的簡報檔：[Tor Stinksa](http://www.theguardian.com/world/interactive/2013/oct/04/tor-stinks-nsa-presentation-document)(完整版由衛報提供)都認為要辨識Tor的使用者困難重重，在透過人工一一比對之後能真正成功辨識出的使用者也只佔了極小的比例。這樣的一個特性使得Tor受到許多人士的歡迎，包括非得經由Proxy連上網路的使用者、ISP受到國家權力監控的人民、還有從事高度隱匿性工作的人，或許不久的將來台灣人也會面臨不得不使用Tor的處境。

講那麼多，那使用者到底要如何才能使用Tor上網呢？早期使用者需要經過一系列的設定才能順利讓瀏覽器連上Tor，這對End User而言是一道很高的門檻，但是現在Tor Project已經推出以Firefox ESR([這是什麼？](http://blog.timshan.idv.tw/2013/12/firefox-firefox-esr-extended-support.html))為基礎的專屬瀏覽器：Tor Browser Bundle(簡稱TBB)，使用者只需要到Tor Project的網站下載解壓縮以後，就可以立即使用而無須繁複的設定。

更新：更新網路設定、從BridgeDB取得Bridge的教學，以及更多的Hidden Service清單。

基本資訊

*   軟體名稱：Tor Browser Bundle

*   當前版本：4.0.3

*   支援平台：Windows (8, 7, Vista, XP), Apple OSX (10.6+), Linux, Unix, BSD

*   下載頁面：https://www.torproject.org/download/download-easy.html.en

#### 注意事項

*   為什麼無法使用Google？我相信這是使用者剛開始用TBB時最不習慣的地方，其實道理很簡單，因為每個出口節點(Exit Nodes)同時有許多的使用者在共享，因此自然會判定該IP對Google有異常的流量。雖然沒辦法使用Google，但另一個知名搜尋引擎[Bing.com](http://www.bing.com/)並未禁止Tor的使用者，而另一個因為隱私權爭議而崛起的[匿名搜尋引擎DuckDuckGo](http://3g2upl4pq6kufc4m.onion/)也是不錯的選擇。

*   不要使用TBB連上Facebook(Facebook有提供[Tor專用的.onion網址](https://blog.timshan.idv.tw/2014/01/how-to-tor-browser-bundletor.html#001))、G+等社群網站：我想大家或許還有印象，有段時間Facebook和Google帳號被盜用的相當嚴重，因此讓這兩家公司先後推出兩階段是驗證的服務，同時若帳號登入的地點出入太大，就會暫時禁止該帳號的活動以確保資料安全，而使用Tor的話很可能因為這點而遭到Facebook與Goolge禁止帳號活動，因此務必注意。

*   不要透過Tor使用P2P：會提出這點並非基於法律的考量，只是Tor的結點都是由使用者自願提供，同時會有許多使用者共享，若使用P2P會影響到其他使用者且造成自願提供者的困擾，因此切勿這麼做。

*   不要用TBB來點擊Google Adsense廣告，NSA當初就是用DoubleClickID來辨識TBB的使用者。

*   相信很多人很好奇，為什麼TBB不安裝其他Ad-blockingc或Anti-tracking的擴充套件？[FAQ中是官方這樣回應](https://www.torproject.org/docs/faq.html.en#TBBOtherExtensions)：「Tor Browser aims to provide sufficient privacy that additional add-ons to stop ads and trackers are not necessary. Using add-ons like these may cause some sites to break, which [ we don't want to do](https://www.torproject.org/projects/torbrowser/design/#philosophy)?. Additionally, maintaining a list of "bad" sites that should be black-listed provides another opportunity to uniquely fingerprint users. 」簡而言之，這麼做[違反了Tor的初衷](https://www.torproject.org/projects/torbrowser/design/#philosophy)，另外維持黑名單，可能讓有心人士有機會產生一組Tor用戶專屬的fingerprint，導致tor使用者被辨識出來，因此官方不願意這麼做。但我[個人傾向安裝Ghostery來防止網路追蹤](http://blog.timshan.idv.tw/2014/01/how-to-ghosteryfirefox.html)，只是在使用的時候會採全部封鎖的方式，不會另外允許某些特定tracking，這部分由使用者自行判斷。

*   TBB的更新通常與安全性與隱匿性的修補有關，因此務必保持TBB在最新版本，否則會失去使用TBB的意義。  

#### 網路設定

在剛安裝好Tor Browser Bundle的時候，會出現NetWork Setting的視窗，一般的使用者其實直接選擇Connect就可以開始使用，但我們這裡就稍微介紹一下Configure的部分

![](https://lh6.googleusercontent.com/WbXwhIKZB3qgvw7de25LmAqCuDz5brUIRRKfud0OL4ItMd3-suVS5wIulN9pUaos7bXmStO6vMN7oyxIicbZOLKzXIJboYLBR2DVoF354mV8dCZXjQ2_VSHWVHMX95wDd0xTIsNMU82ohbBfdQ)

一開始Network Setting會問你是否有經過Proxy，這裡請依照使用者自身的狀況做選擇，一般家庭用戶連線是沒有經過Proxy的。

![](https://lh5.googleusercontent.com/3t-aj_qfuGLAAY9EjE3irekHDocBdEmqzKHIPDZ7ibs5M62AleNo1FtpDhopiC1V4xjP-nl55yAq4WYbM0mFDLgxnh3JlmfHY8IsHLStQXm7B0_R-vp8zCNjqrylF0fBkegmLdzqMeJXvZVkiw)

如果你上一步點選「是」，下一步就會要求使用者輸入Proxy相關資訊。

![](https://lh4.googleusercontent.com/D2flDllSKWidun_7qtDzUYEm2TQxMm-g8jxlHFL7DJknBfwV8LfsBR1zSBD7CSOrDdYq1q7A7eb4ZRxLShVVm77-C6YfelDuck7LNRR3mrpXiYL8bkKhWIa_45JdA5Ws80GmoOXi3BwWDd6NTg)

假設是否有經過Proxy那個問題選擇「否」，下一個問題是：你的網路服務提供者(ISP)是否有封鎖或監視與Tor網路之間的連線？這裡官方的建議是這樣，如果你無法確定這個選項的答案，那請你選擇「否」。假如使用者選擇「是」，那接下來會被要求設定Tor Bridge，這會使得到Tor網路的連線更難被ISP封鎖，但相對的是比其他Tor使用者犧牲掉更多的連線速度，對此Tor Project團隊在[官方文件](https://www.torproject.org/docs/bridges#FindingMore)中提到[一種可行的解決方案](https://blog.timshan.idv.tw/2014/01/how-to-tor-browser-bundletor.html#002)，那就是透過[BridgeDB](https://bridges.torproject.org/)來獲得Tor Bridge。

![](https://lh5.googleusercontent.com/jfRTWMgTmJEvia0JXeNBMcwATJOupJYwjIhwlXubVMQ9NY4OQK3zNBXS1g-LOXxlFmfjSb8pIo7BVTfOLVn5YDM-CGjGzqEYiGBRM-AM-EzTHF2CIcgYTtpiz7IWsxWnd_v3oE5GstejgKC03w)

接下來，使用者需要選擇使用的Bridge，官方建議使用obfs3，但另外還有Meek-amazon和Meek-azure(微軟)以及Meek-google，至於使用哪一個就由使用者自行決定，如果是在中國的使用者Meek-google自然不會是選項。

![](https://lh6.googleusercontent.com/83cM2fe9dqdu3LqnBO9ypJW8rssNEZz6HQeCVPNRfOFFNuQSD_J3G8LRMPtuodCqRR7RNAVQjNSB7vWZeOJXNudS6UM5fGk0r-Qk1WpsGBvvdbqkQ7bNlBLGM4CkX41cGcYRGgJ99LISp_Eacg)

按下連線之後就是等待了

![](https://lh6.googleusercontent.com/6SJIAmuRteJ4QtCRpTSBoIjZ37kTmunqnzWSq5D3ojb4yvAYT7nQP7SFLFTvNrsTcKpHIhWDHcwqQE4we4wz3CJWQRyI5_25Nrgl4SmdT8908YGTOHgrTRSZmQHJs6US-XeVCctjDXxhntZSQw)

成功連線到Tor之後，會顯示如下圖般的About:tor頁面，但如果失敗About:tor就會是紅色的。

![](https://lh6.googleusercontent.com/a5oqrZQAZ7Y4AGmIzqT7IFqrioOHw5OVstBZwMkyPX0YN2xAyj9fLe3Ekxdj3CJGf2ksXDaVjU9JahULfz4E24cGNyfKFK0H0eYaXj_8hW5uIBt0PMST8w4pjDSgvJHtM0dqJ__bQuiGv7pw4w)

如果不滿意方才的網路設定，使用者在Tor Browser的畫面，點一下Tor洋蔥的圖示，然後選擇"Opne Network Settings"這個選項。

![](https://lh3.googleusercontent.com/sGe1QiFPF-12gum4epQD5kdqewyFAjuh5ll_P7lMdV4ebkZ7r1dEMsxECQYRuWUErLzA9s3A5ARHvnVnMd46d3XrQKH4sgBq9WcVrkAMSxCSzaGgV7oQNw_hWMmB8e0rJFavlWaN7UTOo3d6Lg)

這樣就可以依照自己的需求調整設定了！

![](https://lh5.googleusercontent.com/hQWU0O55f6YQJBSKEpD-aC5kOW6iCAvpafOwO1MrbJLm6xhbk3fEfm42AsT-FP4qs2dEVDSCj2Bgdcw687kTvbesXXylbdWtIOA2cLRFLom2ZXK2QYHQr6c7k7grhkUFDsBGQp0lQfRCbwL_ew)

#### 透過[BridgeDB](https://bridges.torproject.org/)來獲得Tor Bridge

前面提到，為了使得網路監控更加困難，Tor的使用者會透過Tor Bridge來連上Tor網路，但是有Tor Bridge使用經驗的使用者應該很清楚，Tor Bridge的連線品質不是一個慘字足以形容的，對此問題Tor Project團隊建議使用者上BridgeBD取得Birdge來改善連線品質。

1.  首先連到[BridgeDB的首頁](https://bridges.torproject.org/)，然後點選一下步驟二：取得橋接(Bridge)  

![](https://lh5.googleusercontent.com/KAnKFqRb44ip6leJ0934mHYTC0dSkH9cdl8iyaiUxVYOCkjsBWh6cwHSXz-V993FHRqQTCenmN4TGb3IloV-596cUcj3fpLqsp92f9Ui20f1jp5SmxLeP-q847cdnUFijh2GOlEm0c05dP7Ksg)  

2.  在取得橋接的頁面，建議使用者選擇obfs3這種Transport類型，在中國的使用者則要注意千萬不可以選擇obfs2。  

![](https://lh5.googleusercontent.com/q_ZwMtGZRVIRkKZ5G7X3yIqTis2xlZbWlpa3Hsue4t3qwmnWaOMSizSBW5fNUejyZ2xXUGb5iL8qvOaqTJuAxrpir2ndsiLifrUew7haTxV2Wpk-k8OF1ipf7rlZOj8EXPXAWLJ3vzKs_kNjTA)  

3.  為了預防有心人士透過機器人大量取得Bridge，這裡需要輸入驗證碼。  

![](https://lh4.googleusercontent.com/7Jv6Q4jI-dza_8xuycmDUozElavRXy3_XkHHs50fYkNPT4l_DEoUvYYLhGv699N832A79IL1BoL-R3uN3yOA_gQ5zI97MtMmaIosWSOApVPZshfFjjKgJKjCmywDFP1YXpNmKWsUNT3RIOFXNA)  

4.  這就是我這次獲得的三個Bridge  

![](https://lh6.googleusercontent.com/VCYMX9wwBoVZvvismHRYAVITSPeGbMKHMGYwkSlN58PCDbbeHfBHi6MVrXvBjPH11ta8SkpIyST9gAqLfuYgQDfDwzH1sv8J4OVGvYSj1QpeOr5sPb0P-N62fzK4LSUNyOcUSz93D2-oHM0xSQ)  

5.  接下來，在洋蔥瀏覽器點一下Tor洋蔥的圖示，然後選擇"Opne Network Settings"這個選項。  

![](https://lh3.googleusercontent.com/sGe1QiFPF-12gum4epQD5kdqewyFAjuh5ll_P7lMdV4ebkZ7r1dEMsxECQYRuWUErLzA9s3A5ARHvnVnMd46d3XrQKH4sgBq9WcVrkAMSxCSzaGgV7oQNw_hWMmB8e0rJFavlWaN7UTOo3d6Lg)

6.  勾選"My Internet Service Provider (ISP) blocks connection to the Tor network"，然後選擇Enter custom bridges，然後將方才取得的Birdge貼上，這樣設定就告一段落了。

注意：這裡每一個bridge必須獨立一行，否則會無法正確讀取bridge。  

#### ![](https://lh6.googleusercontent.com/LeJlohzVdqv7_3WTxzUcw1ibFOpNoFPJWSwK1y7BplGME75Ay3YinbuleEqn_GC9KdKjCc7bFiMIWsuA_-Uom1sp-R0YNwGoDl_UueHR2damLhdlDYIZHkiyMTPKMoYxTVL8XCP6iQnntcO40g)  瀏覽器設定

雖然Tor Browser Bundle已經順利連接上Tor，但在開始瀏覽網頁之前我們還有其他事情要完成。

*   NoScript

相信很多人跟我一樣，剛開始用TBB的時候發現NoScript的預設竟然是允許的！[這個疑惑我後來在官網的FAQ中](https://www.torproject.org/docs/faq.html.en#TBBJavaScriptEnabled)找到答案，Tor Project對這部分的說法是：首先是因為現代有許多網站是需要JavaScript才能正常運作，這樣做會流失掉許多不知道怎麼樣解除JavaScript封鎖的使用者。雖然將封鎖JavaScript作為預設更能保護TBB的安全(這裡就是指NSA幹的那檔事)，但這樣一來可能會增加被辨識的風險(透過白名單的Cookies與黑名單的Cookies進行比對)，在安全性與隱匿性上TBB選擇了後者。不過就我個人的看法而言，NSA才是TBB被辨識出來最大的風險，因此NoScript應該要預設封鎖JavaScript才是。不過在FAQ中我還得到另一個重要的訊息，那就是TBB現在是[可以與Sandboxie相容](http://blog.timshan.idv.tw/2013/07/how-to-sandboxie.html)的，在3版以前的TBB是無法搭配Sandboxie使用的！

![](https://lh4.googleusercontent.com/tykjhdIWZBZD-LMVPPUDi6ZQqszTquAjAO6i37nSx7-3wbOwkussRHfMOvtS0kmUTf3g8QmorDnq1JUp5S0XLzBlVqrUA5_QqB1H4-I37teti6PQ-xkMHeOYc5XngewP6_5cjXqaObmKMRG--Q)

1.  接著我們來NoScript Option，在General分頁找到Automatically Reload affected pages when permissions change，並將這一項打勾，這樣NoScript的許可改變後會立刻重新整理網頁。

![](https://lh5.googleusercontent.com/ncNt_tTqirnFhWAQbGFKWD5kwDMhdFU9sTvFyq7VAiMgYyncJMvEDiEIlDDPHUOb1nz6Fxywl2z4wHdvYJi1EyEkEhVaFSnx1I6JNeFsYLWWqkY_mQDoeqrcR35dnlI1blhQOPVsLEdl5n9XhQ)

2.  之後在Advanced分頁，找到其中的HTTPS子分頁。在Behavior的地方，有一項是Forbid active web content(主動式內容) unless it comes from a secure connects，這裡選"When Using a Proxy"，可以避免主動式內容在非加密連線時洩漏使用者的隱私。

![](https://lh6.googleusercontent.com/p7oK2WUNmAmBWjr-UgzwuMkFvk1dU_0lxUxr6nnaHt4lG_bPxwziunBftL7ZnTgm3gPdZVFnb9mUJcZFcuX831Bxo4DcNH_beOA3v8yAj9zZxsfFfNjkUYza8ZCA-emGo-j_l1LtiGAx-dEdRg)  

*   Torbutton

Torbutton Preference的部分，我們直接看到Security Settings分頁：第一項是讓TBB保持在隱私瀏覽模式，第二項則是停用一切瀏覽器外掛(Flash、JAVA)，第三項是限制第三方Cookies的存取(所以與G+有關的服務都不能使用了[可參考：])與其他Tracking Data，最後一項則是TBB為了要避免瀏覽器遭到辨識而進行的細部修改。  

![](https://lh3.googleusercontent.com/ClAJWz1MtQQKgjRzqlwVp8jsCrUwZZVURnV3P0Bjug_X_nYM_gLDPbmtcqyBxPkpxYr8t-ZhgX7HaLb-6uyer1MvOCJGSi18oFu4wXrXIDCg6dYiek9mDOiYfOQJGmVw7uhzHGMkbQppCz4qsw)  

*   HTTPS-Everywhere  

在HTTPS Everywhere Preference這裡看SSL Observatory，上半部是對SSL Observatory這個功能進行說明，內文提到啟用該功能的原因有二，其一是可以防止中間人攻擊，其二則是當使用者在不安全連線或遭到攻擊時可以得到警告。因此我建議使用者啟用SSL Observatory這個功能，並且選擇在使用Tor時檢查憑證。  

![](https://lh3.googleusercontent.com/ApgAo29ikdwaUxrSwVwoqzs9QSoMUjfrQWKaXYqfogUlkW-Pt_NjXaLb6y0Vhq8JBgNH9204NkAi7_H5XfpQQPTul1QfVFGY9lwJ8MGzq-LB0YXAasEDEKnia5MPiYSsZD0fhemfLYuETrEzxg)

*   切換節點

在TBB裡面最重要的就是使用者能切換節點(IP)，但是在新版TBB裡要怎麼做？點一下TBB上Torbutton的洋蔥圖示就可以了，或者對洋蔥圖示按右鍵，然後執行: New Identity  

![](https://lh4.googleusercontent.com/JuivZ9ZnIV0zh48LYhozcwN8kDzxED1jCezM5C4BrMBR4hz9EJ2f1RBh5qgX94H9QXE54idCx21OwZ39FcIqUaSnXHq9Wr1-l3IWX1fwOIAo5IVUBs4l-2kZOmcV7M2nIEnGgaiWoKAFHgPtCw)

#### Hidden Service

如果各位還記得我前面所講的，Tor的目的是建立一個不被監聽的網路，但我現在所介紹的TBB只是Client端的部分，其實Tor也提供伺服器的匿名，也就是頂級網域.onion，只是若要存取該隱匿伺服器的內容，Client端也必須要使用Tor才行。這種做法的好處除了隱匿性之外，由於不需要公開的IP，因此在防火牆與NAT背後也可以正常運作。很多Tor使用者其實並非是需要匿名的網路瀏覽，而是受到這些.onion底下的Hidden Service吸引才使用Tor的，畢竟這可是名符其實的地下網路。以下是一些比較有名的Hidden Service：

*   TorLinks:.onion網域的網站目錄: http://torlinksysgthcbz.onion/

*   Onion Url Repository：洋蔥網址庫: http://32rfckwuorlf4dlv.onion/

*   Hidden Wiki: http://zqktlwi4fecvo6ri.onion/

*   Torch：專門搜尋.Onion網站的搜尋引擎: http://xmh57jrzrnw6insl.onion/

*   DuckDuckGo：匿名搜尋服務，並非搜尋.onion網域的搜尋引擎: http://3g2upl4pq6kufc4m.onion/

*   SMS4Tor：匿名的訊息加密服務，當網站提供的連結經開啟，訊息將會自動銷毀: http://sms4tor3vcr2geip.onion/

*   Facebook：臉書官方專門提供Tor使用者登入的網址: https://facebookcorewwwi.onion/

*   The Tor Library：Tor世界的圖書館: http://am4wuhz3zifexz5u.onion/

*   Mail2Tor：免費且匿名的電子郵件服務: http://mail2tor2zyjdctd.onion/

*   SIGAINT：免費的Squirrelmail服務，不需要Javascript: http://am4wuhz3zifexz5u.onion/

*   Img.bi：使用AES-256加密圖片的圖片存放服務，縱使是直接進入伺服器的人也無法看到你上傳的圖片: http://www.imgbifwwqoixh7te.onion/