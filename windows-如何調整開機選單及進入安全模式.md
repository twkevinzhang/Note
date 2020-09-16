# windows-如何調整開機選單及進入安全模式
###### tags:`windows` `開機選單` `安全模式`

 參考至:
  - [[pixnet] 如何調整開機選單及進入安全模式](http://george017.pixnet.net/blog/post/111217963-如何調整開機選單及進入安全模式)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/1.png)

## 簡介: 

自Windows Vista起，調整開機選單不再是利用Windows XP時期的boot.ini了，而是改成在命令提示字元中使用bcdedit指令來編輯、增減開機的選項、功能、介面與名稱。而隨著Windows 8的推出，使用者不再能使用F8來進入安全模式；本文也提供兩種進入安全模式的方式供使用者選擇。

對於Windows 10 1703版的使用者，也可以參考筆者在「2017 Week 3雜記」這篇所做的補充。

#### 安全模式: 

安全模式是一個減少背景程式(包含一些類型的驅動程式、病毒、惡意程式等)預先載入的特殊模式，因此可以用來進行移除程式、掃描系統等作業。安全模式也因為這些特性成為使用者自救的工具之一。

#### 開機選單樣式: 

自Windows 8起，開機選單多了一種比較現代的樣式；在這個樣式(Standard)下，預設開機的那個模式(current)會有比較快的啟動速度，然而其餘的模式則會多了從BIOS重新跑一次的動作(和重新開機的差別在於不會再次出現選單)。而傳統樣式(legacy)下，每個模式的啟動時間都差不多(主要根源於系統本身的效能及啟動速度，如Windows XP在開機階段只會使用一個核心/執行緒)。

#### Hyper-V虛擬機: 

自Windows 8起，Windows系統中內建了Hyper-V虛擬機技術(可由控制台開啟，或是在安裝Visual Studio的過程中被開啟，前提是CPU要支援某些指令集)，然而這個技術會與其他種類的虛擬機(如VMWare Player、Oracle VirtualBox等)相衝(不能同時開啟)，而且這個虛擬機是一開機即載入的。您可以選擇由控制台關閉這項功能，或是參考本文特別創立一個開啟Hyper-V的開機模式。

#### 多重系統開機: 

如果您同時安裝了數個Windows作業系統，較舊的系統在bcdedit指令下也可以進行一定程度的修改。

如果不打算使用其他工具來調整開機選單，建議您依循以下的原則: 

1.  先安裝Windows系列的作業系統，並分割出足夠的主要分割區(MBR分割有著最多3個主要分割區的限制)。

2.  因為舊版的Windows系統無法辦認新版的Windows，所以請從舊版的開始安裝。

3.  帶Windows系統安裝完畢後再安裝其他類型的系統(如Linux)，因為Windows本身無法辦認其他類型的作業系統。

## 本文將介紹下列項目: 

1. 開機選單的名稱編輯

2. 開機選單的樣式切換

3. 關閉Hyper-V虛擬機的方法

4. 建立啟用/不啟用Hyper-V的開機模式

5. 一次性進入安全模式的方法

6. 將安全模式加入開機選單的方法

## 操作本文的流程時需要: 

1. 一個擁有系統管理員權限的帳號![admin icon](https://lh5.googleusercontent.com/fUxW018tfzxx0q6ShGuisZQDXkZgHqEAz7vZvdm9--oIirFsvysvIR2q8BvPKAJ4lB9nxl3WVAb7pA7t17w2IlITy8eZOBbyvsfIRfHCRcRYVqG5Sc2_1U5wdgAbTmyG_bmGc2nw "admin icon") 

2. 命令提示字元![cmd icon](https://lh5.googleusercontent.com/hCiW4XnONPNwmAzoMrijlssbROc5OcAvAkNwU0F54TVBpK7hYohuAu4jFAzjFtFY8rD94T_XStp1viTU5nRHwuYePcD3v-jFzpYxybPmHsYEt2b1WvLSDH3fdbwlOBRTdvYlaCav "cmd icon") 

3. msconfig 設定、boot.ini 設定、Windows 功能、Windows 進階啟動![setting icon](https://lh5.googleusercontent.com/r2ijTcQB2ljoPYju9ZqaWBnWFIJBUn98Cm-KNN6CELYFU10vfhIdSFfe2FnuKpsL5ICXFjfV6hjbxKt-cyeWBzpTlG_F-dGO49Ow7CDMpT4AyR08LUsm1C5IsAq6so5rYaGzFFF- "setting icon") 

## 本文適用的系統: 

Windows XP、Windows Vista、Windows 7、Windows 8/8.1、Windows 10或更新的Windows系統

## 操作
#### 1.開機選單的名稱編輯

1. (a).1.首先請使用具有系統管理員權限的帳戶登入系統

![btmn01](https://lh3.googleusercontent.com/8DVwtJM2CPtQHPqngUaNdcdId5FNErvy_KpfnEG233C37eOlP8GpTXVeNtB2QHuMXAg86-Ik5C3hIKVpcplMo7tI3upGeqR4n7de9Ct9WqTzt1ZRzZcOJn4p-Dqemgqyk08SVN_I "btmn01") 

1. (a).2.對著我的電腦按右鍵，選擇「內容」

![btmn02](https://lh5.googleusercontent.com/HRx4tzbKr7GBbm6A4quPJOeLE8aj1zfk1nUkILsgDehVgSrl--k3DWsm2VaavfpbDm1fZsv-7bO01SXCXY8eldThK8tUd1wLIQ26LQ10lgmaaagaeH1N7N00xtHwbSxb3Ec1PRWC "btmn02") 

1. (a).3.選擇「進階」標籤，然後選擇「啟動及修復」中的「設定」

![btmn03](https://lh6.googleusercontent.com/WX6-YkaEY7FJVytRas3H8FphI-SGVkjKj20VWpbSetsB9grNcyid69HqJ5fHqF33q_5JtNnSBK-iZsV6VVWqjMFq-0M0CCr61QS9COJpepFA4fBNnp6tjue2cXNo4gfRqqOdxYen "btmn03") 

1. (a).4.再選擇「編輯」

![btmn04](https://lh6.googleusercontent.com/wjpi7d-XgcgcVCYMPKeF4tfynU-lUAuIgaVNs2d0xd-VyFwwD51_KUjxJaUtku31DyxWZWVVDv5nb8obhpxoq7Hxm9yXj5yXGAtLPjyDDin0sD2S82kMV6w1MU0IEdnxC-NWv2ly "btmn04")

1. (a).5.顯示出boot.ini的內容

![btmn05](https://lh4.googleusercontent.com/I4hAlrPEgibMnZzzB5BusTsy-V0UDIDKq608J-ayMLjyufm3YFEIt_oFrM3mKPag5v8fdVVjj5gFsA7sPeRMujmnCPCUN5uxHl2PrkufeufsDkXkAaIbC5lTwu0rWjOapydxVmpk "btmn05") 

1. (a).6.直接修改WINDOWS=後方的字串

![btmn06](https://lh6.googleusercontent.com/w9IVj3vB2Ga6QAAHEDwwYDfzVYwbZ7JVgaQx01XnTeUmuiuzpeUJhOG6RMT47H6X2I6toSUgMuolSay5LpmwKIw7UyLjQkrCJDxI4Zq6jfKJ4wWL8POEa6sRdcD1FF0uUti3INzL "btmn06") 

1. (a).7.按下「檔案」、「儲存」以完成變更，然後重新啟動電腦。

1. (a).8.修改結果如下 (只有單一開機模式是不會顯示選單的，這張截圖使用了雙開機模式)

![btmn08](https://lh4.googleusercontent.com/oPofNecJY6DgPpO4NqwXgMyFcFs662K3y2PpR8vUXWgNndGmt_ZwBfE1UbhzKvCWCxU85xC_wYeGIflOW7GzqEruMRwtKjzc7XBU7ENxZ1eRJv6FYwGbWW0Es8JwFtbVTvNcR8OG "btmn08") 

1. (b).1.首先請使用具有系統管理員權限的帳戶登入系統

![btmn14](https://lh6.googleusercontent.com/RI1tswUzulsNzqEz8GZ_jmlA_U1KjY90hBYWcSglJvgTcg6FNodXhdhOM-cJ6vNjEpd1g3IzHCX8aoULW_wM7pXJga7WFQfvOCg0sshjn3HrL_Qqunz68eUVBRUohFLqCPV2e6IU "btmn14") 

1. (b).2.以系統管理員身份執行命令提示字元

![btmn15](https://lh6.googleusercontent.com/9YQQnefImMjrmboU07FLs3d6dztXJyax4mTvhoQfiew8u-xSRhQxIAT9OzDFF6uyuqXPVUX8iQg7ysdFLwigOaj5COCdJzzypwIZ-gi4ykv5ogIrconda5yV6Lc96YrdI6GYooKm "btmn15") 

**您可以在「開始」、「附屬應用程式」、「命令提示字元」、右鍵「以系統管理員身分執行」(Windows Vista/7)**

**或是對著開始按右鍵「命令提示字元 (系統管理員)」(Windows 8.1/10)**

**也可以「開始畫面」、「所有應用程式」、「命令提示字元」、「以系統管理員身分執行」(Windows 8/8.1)**

1. (b).3.輸入bcdedit以顯示所有開機相關的資訊

![btmn16](https://lh6.googleusercontent.com/V2WLXfu4WKHU9tCCdsADtuLV-qfDU4mpnlLKZUm6jyPkFa_L3JcmGwXnnLaKp-CaHgZpRB4CEbzMrcfhmYzflr4Rn72MZqKpepEyrv5RaAA77CV4RIcUPAHVj7EpWFQtCz1CFUO7 "btmn16") 

1. (b).4.顯示的結果分成「Windows開機管理程式」與「Windows開機載入器」兩部份

![btmn17](https://lh4.googleusercontent.com/SK4vaGWXTiQP12j5tyjwjElhCKjwRJR945FWiIt4u5QdyKTBZ6Lj4em0CyeusVxz_ARCk0tl_obg5q8WrwBHuakOZREDwOPKsWhDDF7qmnitLqRYjUS4geEo2uZldX4rOisfQ_7f "btmn17") 

![btmn18](https://lh5.googleusercontent.com/SoAct7nbrSYXyl3nnpnh3iaRXSU5yQ2oWRKUPrjgbM_YXpqHg7XU-LU9tKEUKXmBiaHPcDfdPrSTBXaoEHX9X_ZoklBSE4tS6s94PoSW3sTj38yX6CpTyfxq3QpqmQjJWRPGLt1s "btmn18") 

1. (b).5.我們先注意「Windows開機載入器」的部份，我們所要修改的目標即是載入器中「description」的部份

![btmn19](https://lh5.googleusercontent.com/1HfZS2pgLNB7-BM767ft_54ujaSE8GtLsIdaKzxBGwPxvrYorO1u5xEnJ01JoicNbuzjqDQSy_NFsgnV0htgxkiCIdOU0nhcZMvBLMn-lBfP0wqMPFUstIfPopWo_v_5JaPFCJ-i "btmn19") 

1. (b).6.而「identifier」中所顯示的{current}代表當前正在使用的作業系統；如果您使用多重開機，多個系統中較舊的系統(如Windows XP)，其「identifier」會顯示為{ntldr}

![btmn20](https://lh3.googleusercontent.com/J9yVAJQzx1LCxsSXVZ5UK1_W52iV2RNaTHiCR3cPQRYXCXVYibogogMB69hDqikFpNO5cnPonkE9ixKyxBfvXoICgMSL5GyLYTb9RAqv3gDGRBzzBul1NmTK2PZCXTnwEbBbKHjA "btmn20") 

1. (b).7.而bcdedit用來修改開機顯示名稱的指令為︰

bcdedit /set {identifier} description "你要的名稱"

完成後按下「Enter」

![btmn21](https://lh4.googleusercontent.com/vAzgqzWyrEBo_C4jYYwR8zNm-uwB_ajYX-I2p1tMGl6nlkXBjRJqaWtsvVqy-mFn6XM8NYn5Ii47pvlKxa229PJdLCpUT07Fdvy3IW0Ie8l7eaU-yYdEGv1D7FjNzkaY3xixTn_P "btmn21") 

1. (b).8.顯示操作順利完成代表成功，可以再次輸入bcdedit查看或是重新啟動系統

![btmn22](https://lh4.googleusercontent.com/kcbf_5CP9Z3rWyvWrLg1calmX5tqJ753FexrLglIhs7HDx-71VWMFcQSwiZNXesg0OejaxQqrzVeBbqw-48gBxFI82ZwfdkqiDMobnf0bCtVwwBeQIajNm6NKmUeyZPiP5S8tJeh "btmn22") 

1. (b).9.重新啟動顯示如下 (只有單一開機模式是不會顯示選單的，這張截圖使用了雙開機模式，如要在單一開機模式下顯示開機選單，請輸入bcdedit /set {bootmgr} displaybootmenu yes)

![btmn40](https://lh6.googleusercontent.com/I3V7ZhsodjZYrQivDrPl7CwNALE7O-7w3TFN2wbqz_UgmotC3P6XATOizaP3UhGweSTEDOMpXEwUDK4qHR3VKFw76kV9VFuPzuIkZGYVUkfgO68q3Q5gDpXHbMLUNkadSoIOyrnl "btmn40") 

#### 2.切換開機選單樣式的方法

2. 1.首先請使用具有系統管理員權限的帳戶登入系統

![btmn14](https://lh5.googleusercontent.com/NFbn7Wtwy7Yg4I5KEoy1NcNnDWsj2ZyRGSbkjXHYbv9HxruEf4o50DAYhk29G7PUSM-JMGGjmT2zAuonGLH_ezxvkPuBWqb90gJa4HQs3orcsptAjV7-UHB4vEW2Png-ZtO3gP3B "btmn14")

2. 2.以系統管理員身份執行命令提示字元，輸入bcdedit以顯示目前的設定

2. 3.使用下列指令來切換開機選單的樣式 (預設為標準)

切換成傳統樣式: 
`bcdedit /set {default} bootmenupolicy legacy`

切換成標準樣式:
`bcdedit /set {default} bootmenupolicy standard`

![btmn48](https://lh6.googleusercontent.com/7bh6R1G95t_6Z-uM11VGI2wHOEBJdThil-jSFGcewRFfqf7Kck9Vevn3lv-piCSoBycTmEDjeuyZDNRZNpJMXirCQxtX0yuL_VYPQOPHa374D-3B__KBCayIZGUeCODTWPmg7pf7 "btmn48") 

![btmn41](https://lh3.googleusercontent.com/4eoyZuyzy4CeRNjGYgMLTgC1PQPK_x2ceYfhrBaxYm1f8KO5GiSVezrZZcoJ6ePPfPe0Pr9LU0voaEr52Ya07zvMB6uRCzf5KZDZcepEwXqGquAdCePLrpW2GL6iIXyRfnWUc5aS "btmn41") 

2. 4.請關機後再次啟動 (不要直接重新啟動)，使變更生效。

**2017/05/17再次測試，在Windows 10 1703中，把2.3指令中的{default}改成{current}，然後 (直接重新啟動)是可以成功的，所以如果用{default}無效就試試這個吧！

關閉該開機模式中的Hyper-V

開啟該開機模式中的Hyper-V

    safeboot:minimal/sos/booting/noquiboot

    safeboot:network/sos/booting/noquiboot

    safeboot:minimal(alternateshell)/sos/booting/noquiboot

    bootlog

    basevideo

    safeboot:dsrepair/sos

    debug

#### 3.關閉Hyper-V虛擬機的方法

3. 1.首先請使用具有系統管理員權限的帳戶登入系統

![btmn14](https://lh4.googleusercontent.com/LKvj1RweGMVLob4SD_Xt3_YaD3h7bI38bbs2P7CMfbd_-O1CrJ5sl3E70jLp2xeNogltO1VG7oJKSe9gZCCF8Tve9jeian86nP0G4Gg8W8c0W--BL9HiajBZ35JJh0-Wg15h6K08 "btmn14")

3. 2.請進到「控制台」、「程式集」，選擇「開啟或關閉Windows功能」

![btmn23](https://lh4.googleusercontent.com/b39SyDNYzHyu9dgIutW_ZGrYqF3gFOt7c6yxCbAG4XM4xR47edxeE4955jBNKRX7v8OHcs__qFtAYXiNk1iT5iAN-sTNqWGgoqgBYaMAE0SN5kJ95zbCAfyOpu4es_BV6mK7TwBV "btmn23")

3. 3.查看Hyper-V有沒有打勾，如果您不需要這項功能，可以把它勾掉

![btmn24](https://lh6.googleusercontent.com/6Fg4mniE7InxVB0Q76MAI_sE9ZWfgB3hF37Qp1UyYsB4YrCF8x8E2GQMq3ezakfKZ9wEvaXNtz7A6TMSQnu9vx4jxz6yyonF12gWihgIvDkh8cpamtvtUE5hyvJj1fgy3ulZzII6 "btmn24") 

3. 4.您也可以透過bcdedit指令來查看Hyper-V是否有啟用 (見結果中的hypervisorlaunchtype)

![btmn25](https://lh3.googleusercontent.com/RTBtcLlyqwrtH6eOx5LgOePc_t4BFvc5TYedHfmiZQti1qWS1nRTWmo07x8S-C3dFI3TP8LsXJTqjA_Q2XCm0i9OQXbDQELrVnDWkWd2k80QSMDAr6-Z9YnCQ-t8WucglzVMVz69 "btmn25")

#### 4.建立啟用/不啟用Hyper-V的開機模式

4. 1.首先請使用具有系統管理員權限的帳戶登入系統

![btmn14](https://lh4.googleusercontent.com/5TCYNdfIG3iYsmM1qRLnf2L2HaGMSVmI3JiMQUFFpgPwaw-K3NtES9v02XU4uVbqpl3vwtFTh_h9Wd_ryfPEjemW_Rn0YvoCoWVTXMkwQ4eiSBONH1IBLwIqt8nRso1C1DDO1a5H "btmn14")

4. 2.以系統管理員身份執行命令提示字元，輸入bcdedit以顯示目前的設定

4. 3.使用下列指令關閉某個開機模式的Hyper-V

bcdedit /set {indetifier} hypervisorlaunchtype off

bcdedit /set {indetifier} hypervisorlaunchtype auto

![btmn46](https://lh3.googleusercontent.com/o5YAZKF8tKYQSXGatDcWFCp5Rk6ulu-KMZRym3ioDMw-Mqs0SPI-GYrAb1CQtnJrANT-Va1FgEKP8E63w5Ws_AUxCJcioIP-wnAOj8JYTVyg488uh7dcUm5CWSilg2qoUXeWoq_9 "btmn46") 

4. 4.再次輸入bcdedit，看到下圖的結果代表成功設定

![btmn49](https://lh3.googleusercontent.com/YMBppJWuY1qPRVT8E0tpRUe3c6GSGgM66KRnUmP1YJZVFV_4yo44bCOVXPiv2AOhQ82KEq6cQmWWe2vImJqht4EhOR4D7yjq-dAltToWvquIwZJL2JXuaEvV1g33R1TCDvVOc3jv "btmn49") 

4. 5.然後嘗試建立一個啟用Hyper-V的開機模式，先以指令複製一個關閉Hyper-V的開機模式(可參考6.(b))；然後以bcdedit指令為該模式啟用Hyper-V

![btmn47](https://lh3.googleusercontent.com/gy6NKrW3FMAZ170pIp9MBZrOjh6m4n7y3J41IK7e-F4K0BK1NaH7TLfM46Tmx-TdP66tUKkYQB4lCk7-uXbk5A0RItlyut5PGPSXNS88yXnCbFk6FHJVtJv6AoUODMBy8G5SSh0g "btmn47") 

#### 5.一次性進入安全模式的方法

5.1.首先請使用具有系統管理員權限的帳戶登入系統

![btmn14](https://lh4.googleusercontent.com/DrXMxqldtrbbAuABDFuwnOUV8_vmq0mK72NDwHBpl7a1oo14ZQkJdo5TckMSlNSRk7NUVFgvVL0cQzMDX__HjRVvH2h-Sxeor_FfEdpXi1mxMIA2RXDFN7jKk8-FtkK2oxuBOP5d "btmn14")

5.2.先找到「進階啟動」，再按下「立即重新啟動」

您可以由「常用工具列」、「設定」、「變更電腦設定」找到「進階啟動」 ( Windows 8/8.1)

或是由「設定」、「更新與安全性」、「復原」找到「進階啟動」(Windows 10)

![btmn26](https://lh3.googleusercontent.com/_cigvIDRkIX7FsNd0l7DsWtd56Keuqp1NdwqT63nroRXFS43JkrKOCZwPwtyK--msxSRVp4lLz0szTl8vsiMJaFfPuh3NhYGBngNZLIO_O9s_JssQuMCLR7lh1-6aVrhfQOW_4bb "btmn26") 

5.3.出現「請稍後」畫面

![btmn50](https://lh5.googleusercontent.com/GPP4o9w2Lg2JpkJDFPVmWWE7DGI85nNRBfj7pRsASeQn5GgSArQg6O9WEKfsnyouDdcFEbRLtndepsiLD8QjrdP4mS0Zgeixax_rhH3phzg0rrGfR4Av6mzJPYYl3_UFRwaZ4dvN "btmn50") 

5.4.出現可供選擇的選項，這裡請選「疑難排解」

![btmn27](https://lh4.googleusercontent.com/sIl-b6WjxmnlZa5-NyRgJ3KC_pnakKsQBMO8yQW4_nIscrtfyhvH4Ttqn_tbfEFU3TKvSSl29FP9Q6KDEubE2b_9RjS2UkNEUPf2WqTM5giXXdg8wnMU5t_JKDaSKYPmhOV4I11s "btmn27") 

5.5.然後選擇「進階選項」

![btmn28](https://lh5.googleusercontent.com/93AZn7lK8RZYnbK3IJpEIIkcQwWMfKoGY8neSq_PG3DRnU8YDNQJ6eTmVBBRN5CK_gTqscMNPE0uBGNey29EOFYVNmQ1moZEt42gGVI_01A61udENsBkRRewgNgGUflj-wMhA4B2 "btmn28") 

5.6.再選擇「啟動設定」

![btmn29](https://lh6.googleusercontent.com/GHbjifh9tg4VXpAApqmxcW0V_c__ny6ILq5bKnU0-Vrv9hyakCbHcDzJ9hkfy4j_zk_Hh8Z9onkBX_RdR4YwCH6yjuApBkOfq8eMZj1lmXBb3Kr7fFyngYub7u1ZWep2NOnjFkca "btmn29") 

**正式版應不會有「回復至先前的組建」這一選項**

5.7.按下「重新啟動」

![btmn30](https://lh4.googleusercontent.com/c-QOJwh5gz_X1V3N3BRhALOM1bVjPzNlc3FIeZoVTDC1zfix_4z6om1qvFz2jEx8rQBPl-34ZdLa58noz9j16nZCuFDmw7ijwinyff8d8dl5uG1t_oOFpwE8PRk7y7pug9X6lNnM "btmn30") 

5.8.重新啟動後出現選項，在此筆者選擇F4(安全模式)作為示範

![btmn31](https://lh4.googleusercontent.com/6HCZMZKLeInL4-QwHYDharai5qcJ7WNrPzK3yMQ11YYxlzkkS3uHbYw8Y7Wt8o6WehjfdyCBvIij2Z4A9AwLkZjBpinw2an0udC8QO0EiQMtu9WAqJoeSK61_hwAgQCL8zOnfhCX "btmn31") 

5.9.成功進入安全模式

![btmn32](https://lh5.googleusercontent.com/kjeB9rmaraw7OUEZqp0-2OJ95Ke9H8ZAIxcvP4ETzV0sWdGmuO62Ao7Y6mRipvwD3kP0PAjUFxDbSLcYQ54Rus9EH-WKtOauS-dJL8xbxfALgngMdwTFmU2F3gGjY-VMfJ9wt4YP "btmn32") 

5.10.不過下次開機將回到正常模式，除非您變更預設的開機模式。

![btmn33](https://lh5.googleusercontent.com/14VszYf5Js1abE0U3bUnHZyimj5QlrTJ5Lo9e-DVsBnsfoiVq09WjXI7XJzD-yG-Kj3xsbaxCFBMh_qXGKAP6_KIXydkwpEtz6EfkzdsRhxgJak7Hzooq0FIy4AsLcPN-Ou47gdP "btmn33") 

#### 6.將安全模式加入開機選單的方法

6.(a).1.首先請使用具有系統管理員權限的帳戶登入系統

![btmn01](https://lh5.googleusercontent.com/apk-_zoHKxR-Z55_73kivJNAC0UX_y8gGWm6rTZEs-7biiofm89K1YTSGwYcT3Dx0b9e34jJOIE017-l0begK765-7PEfVaEXo_hSudbcV3jzWAKzZMxvoNBgGzo8f1XuLsuVW73 "btmn01")

6.(a).2.以相同的方式進入boot.ini的編輯畫面

![btmn06](https://lh3.googleusercontent.com/Hx2s0rVKGjmXWjsYGptci0pD4Ss03cNV_vXiMQ-iOTE4nPJnWln3fTXBp9-kjNJLCM4dNZgojaq4c8qrtEDzSQYVNTBAa8lodrIvP_jD42Ucyr8Qt1RAKj614MKokeVqCbN9QHtV "btmn06")

6.(a).3.換一行加入新的開機模式，內容的格式為

multi(0)disk(0)rdisk(0)partition(1)WINDOWS=" 你能分辨的開機名稱" /fastdetect /參數

上述的內容請根據您電腦的情況進行修改

![btmn07](https://lh6.googleusercontent.com/oFsrGPDKq1Suoc1baSFH4i7Snx2NGru_Wf6jC2mLCeyj6Z-PcQpCvSUibyE5WIDddpBjvcMhgxbPST4a8ZbSuOa4-RgrTYep96Ngg396pVKFcfJagrstf7c5pceOefOdrV1oOKYE "btmn07")

6.(a).4.再換一行加入新的開機模式

![btmn09](https://lh3.googleusercontent.com/r873WqO_rCV6LvFiVQOy-l2castQbRN7azlqFcIi_k7fCv3MGjigoNywuY_hPotEeOvXZPlEpE7RwH30rxJ0q54oaNWe5tsiBBiiuNy32fFT23nMDuWmL5WoS13rJ3a4AO6yVNI7 "btmn09") 

6.(a).5.重複動作至您所需要的開機模式全部建立完畢為止，存檔後重新啟動電腦即可。

![btmn10](https://lh6.googleusercontent.com/pTG6DV5GzqVbv0WcnfzfcU7EMgsqpzpyQETFqfXAvjdIu6hoE2vB-5q3wzS3drRBWbPbrgPmRqo0vqHkoalf5wPWGKS1dbeE5p-2qDkdJZ_S6dPG3C0pfsWx8nDfdOLxGo0OAG0D "btmn10") 

6.(a).6.完成的狀態如下

![btmn11](https://lh4.googleusercontent.com/qug2sXGWv2aQUrwhu5nIfRDz6zYrGcBVrPAyivRLTFOg4HTWIe0N6C3yftS3--iqZ0MpLHooN-_5MjEf6Ib8Y2nzY6cbU80n5shnqUepTinKtOOVSGeNamD3FtAvBM7LvKGJgpMI "btmn11") 

6.(a).7.嘗試進入安全模式。

![btmn12](https://lh4.googleusercontent.com/GJUBVSxmzs604RG4_LF2tdujESKFgR0O0Xa1xVaLKB_cjwO7DfIaN3yhIJaCdBdDJC_YWqwo7_dKDwbuDJntJ0nPhlJdTUZySXlwwmJjg3G1dhhSBgkAYX8ArgkEHXvwXA8oEOM1 "btmn12") 

6.(a).8.成功進入安全模式下的桌面。

![btmn13](https://lh5.googleusercontent.com/aogDQSrw8hfzfcgyCaEIFIR4eKJPgPSFTSVy3t_Avy-Gnv2C_u_NGbowDweN6Wdk_5ED-VMGBOHx2DL0xXAgNPBOnms2N5bIrW46SEAnfp5K45K0PugatZ7Aynw8YNxbx2YJrcXh "btmn13") 

6.(a).9.boot.ini中可使用的參數如下︰

安全模式

安全模式含網路

安全模式含命令提示字元

啟用開機記錄檔

啟用VGA模式

目錄服務還原模式(僅限網域控制站)

偵錯模式

6.(b).1.首先請使用具有系統管理員權限的帳戶登入系統

![btmn14](https://lh3.googleusercontent.com/3z84X0hqQCH0Js5Yv0uy7NFMwRBbzcAWwiBqLenflhctJmRVE4CWLmiubWJ5tPFwAPlmNnbzZkulIy9-Mk9ryHJrfeuQwv05kKJjQX--PkNawskW0W8OvDGqQcMSYNychAcrQFT2 "btmn14")

6.(b).2.以系統管理員身份執行命令提示字元，輸入bcdedit以顯示目前的設定

6.(b).3.為了增加一個開機模式，需要先利用指令把現有的開機模式複製一份再進行修改

該指令為bcdedit /copy {identifer} /d "description"， {identifer}所代表的是identifer所對應的名稱 (單一開機模式時通常為current)；description則替換成該開機模式所顯示的名稱。

![btmn34](https://lh5.googleusercontent.com/TSdox8sA8ZBNC2vcd3K2TEg6588gzI5ZoyaXno1FisyJJqdu5piIdNXaj4MwkmhUyutfk8PIx_QCRbJ-dVyxTazR79F7sWfFRKbnJrt7m1NFpz_4x7KczykxKVU_2EFTpb4KolTu "btmn34") 

**當要變更數個有著相同{identifer}的開機模式時，其變更的順序將是從開機載入器所顯示的順序依序被變更。**

6.(b).4.看到已順利將項目複製到{一堆亂碼}就代表成功變更。

![btmn35](https://lh3.googleusercontent.com/pRM9rR-Hf7cGUZ9ppgh_ssKSBfaZyMgp7aieI2Y6BbB5oic-vGGh8QyUIp2nBr1jpNmDHRVOAznT_y-yrkx5BFGNtkoSzOa782cMU2_xjhXcWbSBjUtYoNf7OmY6gHGNkkYsXQxV "btmn35") 

6.(b).5.再次輸入bcdedit查看目前的狀態。會發現多了一組開機載入器，那便是剛才複製的

![btmn36](https://lh3.googleusercontent.com/qPtf6xKvpTJwA1W0Srn_Ur275-_AOC0SWIhKBnQLwwpk5lIZrZ_-nnjKNf-2xL3ImA8zjrRVocpilD44rKe-YjheEqWty1AMNur26KY9SPIl1LiwJQhZqZFEjHQQr-dIfFHoH3_w "btmn36") 

6.(b).6.先將開機模式的名稱修改好進行區別。

指令為︰ bcdedit /set {identifier} description "你要的名稱"

![btmn37](https://lh5.googleusercontent.com/DdQgENAJhHKI9tluav0F-JoJKydy4rRnNLCdeloTivOj0JVM0mXmS_1e7PpOAyv_weARW2SoPw98vyWLMHVgu4Mdr5Un3WwNHo_i2uZLznUreAtyKXYcmUDVeFlSLCtIR_8wW8Or "btmn37") 

6.(b).7.接下來可以使用bcdedit來設定不同的開機模式，您也可以前往「執行」、輸入msconfig，由圖像界面來設定開機模式；在此先使用bcdedit指令進行操作。

指令為bcdedit /set {identifier} 不同開機模式的參數

![btmn38](https://lh4.googleusercontent.com/jfpQ-vmfyN2YoA1F4GiR8Z6XE-auEsNUjY_ukRomeWRMv1C1FmT1CDo7PdwYwHjnLFrFP4ORqVLu5415fL8sSPjg_C_ys4OagFU3sWLkiPU2BRmNyXiov4DHttuX2E_K0N9t8Z1U "btmn38") 

6.(b).8.再度輸入bcdedit，確認開機模式是否正確

![btmn39](https://lh4.googleusercontent.com/cTAhP5X9ks1LK5ukdUJA1OkerZuKHYT91W8sTGVoblorAKZkyloWc7iTK1JwZ6B_I-NUi-9CwkMubWE1mqJnM_PYHtJgWcUqxhaU8v_3ptxmfoy4oglPOpW8U8GQYxBIXiyZDjm4 "btmn39") 

6.(b).9.接下來再複製一次最一開始的開機模式，並且重新命名

![btmn42](https://lh3.googleusercontent.com/kcPOa5br7eABN7JeJEzuZtS2iDx_HpBzw1NuEkK_lPaKuKU8jc0CTVMP6Gv9jzqYShK0b8g77drAT8AzapKNtjRamCIP78e-t-Tb4hKtRoAgXvgzVuOV_dVvaf-vMa73gEA7aMgl "btmn42") 

6.(b).10.接下來使用「執行」、輸入「msconfig」

![btmn43](https://lh5.googleusercontent.com/QSUla0ddTOiwbbaRZx6xWl0ndkdGLpMzEIWbDxk1Q78-kjh2FUu5vzyNerCVFDmK0v6p_1mlANeuZy8e3chHmOEiNKWJDR9crlovHKGeD05i-l6L7n7-bDFua3IU7f9b_Qt2tTVH "btmn43") 

6.(b).11.選擇「進階」、選取你要變更的作業系統，調整開機選項的設定

![btmn44](https://lh6.googleusercontent.com/_uNgCp_hNresMek8T3SDjJalyabM7tnsqp1VC-y3HXoPtCAq2SPvUvfSp134TJgWRXT2eiKSiBYltnYxjp9ppZnJwupRKOZnD6jzwI_vPMK7Dl_OU56ct3_n-ilf53hs0UC-sIq7 "btmn44") 

6.(b).12.重新開機使設定生效，完成的狀態如下

![btmn45](https://lh3.googleusercontent.com/q_q4DVLr_-TCJHuIV1afr0eq1BKCCNwKc35OtympJi2VnOezwqBesnlmE7-G-EzqQbr822OLmnZq741BZHYOPNesFFgaxhFmZFjlAnoWezVDGFpZxUPtHb1il-I2Gw2AkdfB_7kR "btmn45") 

### 使用的工具、軟體一覽: 

VMWare Player Pro 7.1.2  (非商業使用的免費授權)

3. 位元的Windows XP Service Pack 3 (在虛擬機器中)

64位元的Windows 10 Technical Preview Pro 10130 Build  (在虛擬機器中)

64位元的Windows 8.1 Update 1 Pro (實體系統)