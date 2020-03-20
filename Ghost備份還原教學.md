# Ghost備份還原教學
###### tags: `重灌準備` `Ghost`
 參考至:
  - http://brian6724.pixnet.net/blog/post/7052815-ghost-%E5%82%99%E4%BB%BD%E9%82%84%E5%8E%9F%E6%95%99%E5%AD%B8...

(未嘗試)

如果那天系統發生不明問題，或是中毒，即可用此方式回覆到最初的乾淨系統；回覆前，請先備份重要信件及文件。

#### 事前準備：

1、請先準備一張空白的磁片。

![](https://lh3.googleusercontent.com/UyDLH2AjTlLmyZaWwRIyUysOFDeuyoZlyNlhFWQ-1ulIIabHjffYKuTQTztI1HPJpX4GtHq7M6n7XFXDxYAqIyAOaoMnDuVdLXYVdN4BiFyOc7whGw1ag4_tjSulp9JtQwaMdkUU)

2、製作開機片。

![](https://lh3.googleusercontent.com/5NKgV-nilKswniyqhXujJYQgeKDgE3M83d8iaiErST1dzGiL48PukWj7EIbnA4eoj3_i99YCfPGTKSTgBgDk0O8tN6Ymb8_xa-JYbNsMBTBhix72jOkDcd4nk_7uupwrnjuGFN0v)

3、重新啟動電腦，並將開機片放入軟碟機。4、接著開機後看到A： (已此台電腦為例!)這時鍵入 C：然後打 cd ghost再打 ghost5、然後就會看到以下的畫面![](https://lh6.googleusercontent.com/QeyW14nPrWZwNGud_xgi6VHOGPXl27aw-ZfecDomCWtNv6X9RKtwskt_Vz7hLpMytGsTXPEVHZrKSvhjgIY21BUe03nGnZt6UjdZwXYWqr_sNbNZ7W1un7kSENZPaU-SB6gNh1ra)這樣就表示成功進入ghost了；按下「OK」若抓不到滑鼠，請利用鍵盤上的「Tab」鍵，來切換選項。

#### 1.系統備份

1、選擇「Local」2、選擇「Partition」3、選擇「To Image」就是製作成一個「映像檔」![](https://lh5.googleusercontent.com/txTx-iosGlQeHcsUjl5dmCntupIQkOIdF60zSWbEv_z2A7VnMEBy3iZroUTa1kTds9tBf5RmcwNFLOKvA5eWgCgq-K7Vb_0FoHn-g9MS0VpOxr5tyUcKKLCu2VJg2zBu6w19kIaB)

4、選擇你想要備份的「來源硬碟」5、接下來按下「OK」![](https://lh4.googleusercontent.com/-z5dbHDNV2RergHCt_GcMkqmA_N4Dnze6uitLftL6z8g4UJs8ykBYtPh6BfoX3isN7EHp1z1WiuZZLnEzeq38ONscGSKPSZnJcUFVxbR5btp1nXIKFTfiokwHgMYn6eC86yXxGG9)

6、選擇硬碟裡面的來源「硬碟分割」，通常是第一個。7、選好後就按下「OK」![](https://lh6.googleusercontent.com/iFIImkVq2jJZYCv3iXkMzXxdvgyMmQ4PIHyAwwljQCkSWNyzD5sv6BAePPiQ546xW7a9uK1upaSFwHughk8ISNFSDIKtn1grPc1Ks1z8O92h0B2-kny_-gvU2ytFKCLrsZj0yuNC)

8、選擇你要將被份的檔案存放的位置；注意：不能存放在相同的磁區(Partition)中9、輸入你要的檔名；這個範例我所輸入的是」2006_02_10.gho」；當然你可以輸入你自己要的啦。10、選擇「save」存檔![](https://lh6.googleusercontent.com/y00jQKS73NEdZHPIRGLB19G-XukIjlQtIiuAThKzzbeyHnYbBKHMoKV1iEK9ECaccves80iQxr7M8aQvLCR0oI5CM8uKfMWYtf6EG2aXyK47ik9yymUm-qJ_QCSUHXOhgZq8Ds1-)

11、這個部分有兩種選擇就是「High」&「Fast」兩種；「High」是高壓縮但是所需時間長，「Fast」是沒壓縮但是所需時間快。請依照自己需要選擇；通常選擇「High」它的壓縮比大約是1G：650MB，提供各位作參考。![](https://lh5.googleusercontent.com/gIFNk3ZbHSiiP2M-i5V1utpTL5NKMW_ECfTyXwg_wKu5qDFJJFCT8iFJfuPy3RaFZg4HWcZOy73388_xpAwaUhTPrFJZCspZyuWBzB6cMGMqT9OWkOMro4-r0W-YYqJLfO0qok1M)

12、再下來按「Yes」就開始備份囉！13、備份結束後，按下「Continue」就回到DOS的畫面；然後重開機就好！記得把開機片拿出來喔！！

![](https://lh3.googleusercontent.com/oTDKrTUUJX3k_oqo-2xLJCQXKz10F6vhV5ZCWQFFlXVoERdfTkSNRUrhL3rWH25N9YoHKvGQ5yDVlvWGIL1VG_sGUWVl4um5GZVTvu1gJGjtG5QdC71bnmqwTTqqkRDgO-AySVqR)

#### 2.系統還原

![](https://lh3.googleusercontent.com/PHXds89wh3Bkz9I8GicQHH7kd-Ipg8o7MYyWbjfnEhCyKvvWcBazQgkLHpE0R1er8az2ZqDDGTCa00NJLHr9YmkcyYK71i_qV-mhsBgV8qcvdW3DoCYM4M9gNKr2RXQ-g2BpbEh3)

1、選擇「Local」2、選擇「Partition」3、選擇「From Image」就是從「映像檔」還原![](https://lh6.googleusercontent.com/H4y06G9AZYs_pPrR_SPArSFUuozqr3g2atjSqFSypc-b728QVGO4UzIo0P0XN3LHv2mAZ6t-d1vBXjVy9Zk-6xUtjjmVeENXV6Q2U4BqGwAeGlOVnUZCas4KZ-HnekLpdei1gio1) 4、選擇你映像檔存放的位置5、選擇我剛剛所輸入的」2006_02_10.GHO」映像檔6、按下「Open」開啟映像檔![](https://lh3.googleusercontent.com/AeEnF4u4XSg_ak6mcgaoW9wdwLQbgt-U9Xhudy9dvJRfj5laZlpBo9QBYUQ2MdwQPK9HE0UKZy_-tkrgSf3rcWU01ylY9OJE112aqTg3WxgxwuqQm-qL-S806EWK3Pqpvz23wJY1)

7、檢查所選擇的「映像檔」資料8、接下來按下「OK」![](https://lh4.googleusercontent.com/CciY_5p7Mhjn79oOv0d04l3YSYfJAm4_V1RwFCuwjGRUnzVDYpLHHio0xfkXy7_phm5iiJdUzX1bNPKTwzxXQD3y5J3rfuus36hjILd6EPAlK_yqMRXu6s6jQp-wdnLKAg2t7lpX)

9、選擇你要還原的「目的硬碟」、通常是第一個10、選好後就按下「OK」![](https://lh6.googleusercontent.com/Y-WKzb_mOE3eRIzLNDyXblJESHcDFZMzYLl0Tb6bXMY2PThuY5uY2XB2B6Dm0QMoDqadjBbl6kD1sIt4L5YGkcthi79w28-jWj4aEjR31dZ5dQv5P8-JjFGr2Bhp74lvb0DNQpw5)11、選擇你要還原的「硬碟分割」；就是Partition12、選好後就按下「OK」![](https://lh3.googleusercontent.com/o2MnCLVjqIv0MRb2z_uUFnM7hSf1fLdQTxnhtsjuSQvAsxg6V_Li1cQ3J0V0weismTC3WONwkJNQDiPIJwF9HkApKdgGc1NJyanNscnsJUPFO--aj8PPHbKdCR-O99Wb8MmiHzuo)

※這裡是警告你即將開始還原；你所選擇的「硬碟分割」中的資料將會被覆蓋！13、按下「Yes」就開始還原啦！結束後按「Reset Computer」就會重新開機了，記得把磁片取出來喔!!

![](https://lh3.googleusercontent.com/RNa50go5KNpL_lXuPEyw0q3vvYa2gluTf1Ccw-RQcs2t_tQ4JTzb_0FTW9VMR-HfKOSu_5DzL07FWhuTsdjkeeidVFZtVJYHWVlf2DCg75SibMVb0rDatcSRD5n_-NWSVYBY-zm4)![](https://lh3.googleusercontent.com/7nSXwfJWFOaKlSI_C_DV1xpMeSSuf8z9bNDAMyesZtrz7ODKb1iUX70nz0SecwNEPsWubMCk9Ra8w5wkF6V4y1V1jeggaJRMrdTGYRf6Ud3Y39_1d8cmWCg3ghcrTKcaIuf2cE3o)