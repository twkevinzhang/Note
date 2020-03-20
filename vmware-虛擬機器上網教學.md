# vmware-虛擬機器上網教學
###### tags: `虛擬機` `vmware` `網路`
 參考至:
  - http://blog.xuite.net/r413318/justforfun/35138059-[分享]解決VMWare不能上網

    簡單的說就是讓我們可以上網的那個IP分享網路給VMWare用 ，這樣VMWare也就能透過那個可以上網的IP上網了!!

(以下是在Windows XP SP2  和 VMWare6 下操作)

(理論上VMWare6版本以上都可以)

 

#### step1.

先設定VMWare，先到這個畫面，點選Ethernet，來設定。

![](https://lh3.googleusercontent.com/qH3XMtQvAiHbCtYgT9BEZGk31gjXZc9yxcU2Aog2UUn5RRLaZbDQqqgwaZzzPQbnRvyPx2u0PU4G9q1b16X4AD-zCUTJoZrue0CMN1HdQSSSbKaHw7q4BxRUi_NUFKz36ayoARj_)



 

#### step2.

選擇Cutstom: Specific virtual network，並且選擇VMnet8(NAT)這個選項，選好後按確定。

![](https://lh6.googleusercontent.com/gCwRzHe2vB0YkIdUBhFx3qaHqNVDC7rzzYPz67el6PPimiNOwv0Z5sOnMXGo6zwRohvbkMavzXHDhZAIQTyFlOiVXjkv0rS6EA59m7zXwuKyQIaokXPT0_qdxLjVss1uqE81-_yc)

 

#### step3.

我們去網路連線 (網路芳鄰->內容)，選擇 區域連線->內容。

![](https://lh3.googleusercontent.com/wk7uUI70HIleAiC2HxliD-g7T8CkU0jtkwP6NFSGRfT1iU4HsYRL5qy2vpophvkcg3e8V7zP8muBsTJLNkA73eBF42qo3Ts4MH8MyfEnA9ZLZBYh_9ZEjN3AXWzeFNC0ZiyhzfqF)



 

#### step4.

切換到進階標籤，並且把「允許其他使用者透過這台電腦的網際網路連線來連線」勾選起來，在把家用網路連線設定為「VMWare Network Adapter VMnet8」，之後按下確定。

![](https://lh4.googleusercontent.com/GFKOQopbxtVRy5iKlqxcLAGFaQ_gFk0MnbI_1MmooXoX0jo6qBUgJ4MlFnGivqTwr5C6eFVBEYDZBflUfgReK2N2BSOCWTNBfIxpUTR1e6ejOIROhk5MY3NqO6gvKTv2RaOJivCx)



![](https://lh5.googleusercontent.com/tL8jx0fCsrgI09VuzeRrXOQqokyIrSM8b8nMbyLi-H00uRux7VEMvwKlqSUOtdBfzvg45refcVpxjqh7pgVBpj7IkSffCqs9yWrghbG8b_QsUMUgZMzaM925hNlQfxJrA3dU3R5A)



![](https://lh5.googleusercontent.com/8WAd6jZfUKva3BMS1fd5O8gus2bH5dXXiNUBo5WoDZTJbwZ-zlGtQlWdf03EO7MmF7Ov0KRlFMNu3EkEoazSnGQ5-v4YAXfBS-ssvJrjwaINHNL4I4vaJjeIzvx-FTZy1NWYAsm8)

![](https://lh6.googleusercontent.com/RZpzb2DtL6NHc5w8_WZwphKhQL_jk9sgpohHtbXbNjgzuRgOEdGBiXDhmcYu8evtUjFfcBlojteslry66_s9G650fmhiOsmBj7A35J__DhZMkAWuFY6unk5mf5eOQe28ft-8nJI6)

之後這邊會跑出這個訊息，請不用在意它，按下確定。

![](https://lh3.googleusercontent.com/sPWnPcOgkO0glJ6-x9U7CIZ4LID7bIzkcbvsuAXhTQZAMtbe7MAjP4jNwjO2wA3mNaBBUpkrc3HxQlUJzOHfIlNFOT4JS5T5TBZvY83V46XVqgIseomu3pe7VaKppYiLxBuxzkUK)



 

在這時候，我們的區域連線就會多出一隻手，表示開始分享網路。

![](https://lh6.googleusercontent.com/qhvf_BiyCjjAswjkl1kuh92QwPqxRrBnrcQi0ckhWuJGQpYRnLk_QaI6T3cBMKXk_S1qy6lIG3TJ5btBG7m7LhO-GS-XAbWXtvojSx8gM79yI6PB0GM-tK7DsHtYdkZ_K9yf6uZA)



#### step5.

選擇VMWare Network Adapter VMnet8 -> 內容，再選擇Internet Protocal(TCP/IP)這個選項

，會看到IP位址與子網路遮罩都被設定了。

![](https://lh6.googleusercontent.com/ayU3Qd9gPNagTHc6vr-jUU0f-k_4fmaQE39Xfw9n8jqAvXmnQ7rrNoaFJnl5D0g0QsZ7nRlqfQhbbfnOnvQzBPJs_-W5b-ngT4mDe20HsAWB9dXWSMcAEGFcVrW-IU-cyq4ZYs0J)



![](https://lh4.googleusercontent.com/_5dmGMNXZU0n0XvYFoHGrlnpe5SZsYvPkOZvZ2WbxVnywXO-_--HXuu5BGpMsQ3tUDRfg8nxNppeOhAn13V7wXijc8WpDkxcm-sSpLPQxgYJ51WAiCklizKuuTVJwHpTemi7vzmg)



![](https://lh5.googleusercontent.com/cQ4p123JaX3eUbnjqLH_iSkmaUfi8vzTJqpfG_2RUQK9oH2-UKfwguxQvyd4RyjrsgrqWDxvibP9ZieRJJ4aXCtDAyF6KhRPAvi7sHIt545TphUrOe6gWqP7VpSxVuQGB9KlhQag)

#### step6.

把IP位址改成192.168.55.1 (55可以為任意值)，子網路遮罩就不用改，慣用DNS伺服器給改成168.95.1.1 (這是中華電信的DNS)，設定完後按確定。

![](https://lh3.googleusercontent.com/fvOqev42VRmxlZh-3Gjv_mvQBfNnyXgrPyCJHbhFfa4u8mmSTSKs5ifuxXQo7uY7cTb-jeNuQaRjkF1MjgLRpDo23ZeNg5zmqYLbrE3KTragBpz7syoxkoP4j_FD8OHxkVt2obx2)



設定到這步基本上NAT就算架設完成了!! 再來我們去VMWare裡面的作業系統做些設定。

 

 (注意::  下面是在VMWare操作)

 

#### step7\.

我們去網路連線 (網路芳鄰->內容)，選擇 區域連線->內容，並選擇Internet Protocal(TCP/IP)這個選項。

![](https://lh6.googleusercontent.com/xQ1WTzRl4CwawpKLTt3-ojvthi6JFixSqY5w3L0D9TkyXIJbOfvtjERHZfoMlgFXW0l7LS4EdU93fu1NBsVe9fK0ahhbKVluL-8ygpUyCdm4xq7b389W-UwqNISPk8iw_GSvIDi3)

 

![](https://lh3.googleusercontent.com/gLoAU8WjcwfCtn5i3J6wls5cY657w4_FC6xqkQAGPR7p_RDIkadf7RadjsDmEFuSydp8cbpH0B47cO4Wjdla3Idg2ZfLOHLxb4yVfGT9rigHykGwbB4Ca-hrnHqzaRL-hA4T30oa)

#### step8\.

把IP設定為192.168.55.5 (55就是剛剛給的值，最後的5可以為任意值)，子網路遮罩為255.255.255.0，預設閘道為192.168.55.1，慣用DNS伺服器為168.95.1.1，按下確定就大功告成!!

![](https://lh3.googleusercontent.com/L8qaXQjGhzV6_PZASRJraFKpsCh6Ow0UmFjv4alHFMPeyl0N1myyDUBU-6VnZAe9OucgAM74nz9Yk-oXdZqVVzJyz7wcAgg0L4YJAcx6QfDSmllIr6WFXhlHCwhsgLx_xufynfPY)

 

設定就到這邊結束，VM可以上網囉!!!!!