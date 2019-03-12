# batch-快速切換網路連線的IP
###### tags: `batch` `網路` `IP` `windows` `win7`
 參考至:
[http://blog.xuite.net/yh96301/blog/240237360-%E5%BF%AB%E9%80%9F%E5%88%87%E6%8F%9BWindows%E7%B6%B2%E8%B7%AF%E9%80%A3%E7%B7%9A%E7%9A%84IP](http://blog.xuite.net/yh96301/blog/240237360-%E5%BF%AB%E9%80%9F%E5%88%87%E6%8F%9BWindows%E7%B6%B2%E8%B7%AF%E9%80%A3%E7%B7%9A%E7%9A%84IP)

只要使用Windows內建的命令「netsh」建立自動執行批次檔，就可以快速切換網路連線的IP，詳細操作說明如下：

1. 在工作列「網路的捷徑圖示」按滑鼠右鍵，點選「開啟網路和共用中心」。

![](https://lh4.googleusercontent.com/1lGyKIYUuzrcRUqsvRG80bjQym_vPmpbYehTM7EM3LOHkVamnxZLjOXcQyrcTQ-yeXfENuOL2RLLloMiiZM_1DNRQpjK2rUbVTYpGC9SHjfFk1kEwQIlwHaNn9Pwf5vCsL2lJNnf)

2. 點選「變更介面卡設定」。

![](https://lh3.googleusercontent.com/TcmU8-GJDn22DK_Rra4JJpSd5vw0pBxSnmdvLnfoyCrRi4cUuRgOqUpM9goisOBdGUtzQ_rjpyh0devZ_-7J-slPFKX1MbfX3KuvGQvXbwb6UMFowkoohHC7CGioGOJMgxFA0IDi)

3. 記住你的有線網路的名稱，如下圖所示名稱為「區域連線」〈不同的電腦，名稱可能不一樣〉。

![](https://lh4.googleusercontent.com/sQ3crxDrpsvgVafw0RxYWlA159FhihAnZPpLE8DnGgJgWXoGUeskaO7VISD8f_-m8aSLzKJyuEam9yVWmunSiq_P9ORZCM2s-xtqp7Q3cTXoscrkbdCwQgRNKset9vnnnB8LzOnK)

4. 在桌面按滑鼠右鍵，點選「新增文字文件」。

![](https://lh6.googleusercontent.com/3dTQeZTQZ3gaOB0ZZ7sk88jinO4-mz6XU9AcSq3imAVBhj8ycX9gVmevju6DbeeTiI5Zi44GQB4POhXVkCPsP7poHOW3sS9H4B__J0zvkLsBOb0g8gOYnF5eJN5l2E_UXg2DbJ3y)

5. 直接按鍵盤的「Enter」鍵，完成「新文字文件」的新增。

![](https://lh6.googleusercontent.com/T9mFVLiDlbe9eULB0tuT0rVc3HvHajhXIVem3kFZGgBPaRFWEaNK8zGap8fzzeYhtnpAT2Hkqiolw10-MDgOu8uSogzN_Q58ukaJ8AkWwZ9YSFFgTdS7FBg62-yPera8PM1ypHyP)

6. 對著「新文字文件.txt」連續按兩下滑鼠左鍵，開啟文件。

![](https://lh5.googleusercontent.com/pMMgS2T3W1yv8SRECpbmpHJSm4Iv9yhCmR8SfhLDOWWoemRyPHoADWdcy0g_zx4eWg0R07pWkSh_NHG2VhoQhH9-phWraxb_lqLFppBSOYjZu0uxNdbhaeq2R7ApqX_TMjm0qu3l)

7. 在文件輸入下列兩行文字，將網路設定為DHCP，其中「區域連線」為電腦有線網路的名稱。輸入的文字如下：

```
netsh interface ipv4 set address "區域連線" source=dhcp

netsh interface ipv4 set dnsserver "區域連線" source=dhcp
```

![](https://lh6.googleusercontent.com/Y5OrXSx08fOugSSyEjYGkuVN-wM0wv8t2MYPYb4FOsYZxvU_l1LO75Zg3UXpL3vxuc06xIsUhZ0qkz1pAJ-T-Mf_RSuDivxRi8SkmM72e4kDLvXRxZWAYRndx1AH3QAjoCDAPcv6)

8. 點選「檔案儲存檔案」，儲存文字文件。

![](https://lh3.googleusercontent.com/c4grZUh-ueJrzH6IjvRYXlCrXJt93TPRBiaABe2svul_lyfIZoX4kN9l0hqVIPFVMiDlOayBVs8oKSeR_7XHQTK7QWb1ZA30PuJjD5doIKqNA8S1TPGVt-8tvoLNqcc_J-3uQ5_F)

9. 選取「新文字文件.txt」，按鍵盤的F2按鍵，準備更改檔案名稱。

![](https://lh5.googleusercontent.com/VJlgcY7a1zHiGeB946dtvxyxlIe9WVREE7kyB4Absqc0rWQasNXUIP1ShvxymphDYtXNwTAu7FTZRYDT5JeXgvFVzFa3bmhm85z_fzNW7DnQ9LTuxtaXfHeUKWS8ylmTgYecpWKn)

10. 將檔案名稱更改為「DHCP.bat」，完成DHCP批次檔的設定；名稱DHCP可自訂。

![](https://lh6.googleusercontent.com/U9vqQgIpVb5QtA4-8U-6u9WC7O4UP-8uAwpJ9gecGQXvtFD1ZCwB6ZKp5ZFq0mIAn3Xa9y65LJhY9tYOERxwnz7dg9ixTPnivDJRefevubjIhnPvDqGITZ_OVjSxUrXkA_Of52r9)

11. 對著檔案「DHCP.bat」按滑鼠右鍵，點選「以系統管理員身分執行」，就可以將網路連線設定為DHCP。

![](https://lh5.googleusercontent.com/jIR-93ZBPo76tbp_Pu1kP-EspXBE-dELPLOnWIbtfCEy3VCczZbFGsawO6upeTn3_HAR4u7ExjDe8VsBhlSIUa7YF9aIyCdobRh68EfYgnUIPmOQDaBTzb0EUlV0OwVSFZ3yMAJ_)

12. 正在將網路連線設定為DHCP，如下圖所示。

![](https://lh5.googleusercontent.com/joZScRqTh2xmmk57UT1kOLj1SHO-o5jjXtaLsjvMJeAEpYJM_6vFDq7dKAfqZt6fw3tHoUHAQSf_HVnhc8K0expKCsPTZp3o4TmCacnHELJBWu0o3d67Yzr7_bdhZacH21huXl__)

13. 在桌面按滑鼠右鍵，點選「新增文字文件」。

![](https://lh5.googleusercontent.com/OUfcRZ5JxxE2EO9kJPaaFqws-OgRrbpPOSA6hMmVScm9HSEPrEOflxtQ-SHbX9pYuJFHcY-86WC6K7HjwMEANsE1ussmvC-oPf5si8C-HCLG6tX49Dwp_h7rm5ObnMZ7OJOkBLsh)

14. 直接按鍵盤的「Enter」鍵，完成「新文字文件」的新增。

![](https://lh3.googleusercontent.com/TRtQ9HiU8kCkSYPiHrgPu5oa7bMtpj6Yk3Iu_C0BGcd1UsqKRtoaqBux4FhD_Q7u8bi_eUsAozKsmjXI-sjapWdreryUkw2bDTho_1y1iePAPXvTkx5qo7dc8BJMYQxbiibfxjvT)

15. 對著「新文字文件.txt」連續按兩下滑鼠左鍵，開啟文件。

![](https://lh3.googleusercontent.com/JIMMpn4914up9GRjA2ej4dQ8r1aDXL8aJaPAYASnA_CrLqTeOyejNF38XAGpx3yEJoxh7Pb3mtQkmUmKNXJOOXvs0VttAmwNUj4MG4LZTAGDVZGOxB4NOsRumwEueGwzY3zRXrzW)

16. 在文件輸入下列三行文字，將網路設定為固定IP，其中「區域連線」為電腦有線網路的名稱，192.168.1.38為連線IP，255.255.255.0為子網路遮罩，192.168.1.1為預設閘道，8.8.8.8為慣用DNS伺服器，8.8.4.4為其他DNS伺服器；上述的資料只做為說明用途，你必須填入自己的IP、DNS等相關數字。輸入的文字如下：

```
netsh interface ipv4 set address "區域連線" static 192.168.1.38 255.255.255.0 192.168.1.1

netsh interface ipv4 set dnsserver "區域連線" static 8.8.8.8 primary

netsh interface ipv4 add dns "區域連線" 8.8.4.4
```

![](https://lh6.googleusercontent.com/-KhW7RdZioym9gnXFl2Nz9mpqyqjRbayecWunu_2X0cfdggdU_iOD0vhALwr-LUT8dnyUGtz8QLP03_rSLMUgo6IdAMNLx-NhszBq87XyXwd1YuYfQpvg22EeieJTy-a6xTcDwHG)

17. 點選「檔案儲存檔案」

![](https://lh5.googleusercontent.com/dIQ_akesXjQkNwZ66xISCmJVdXP9Qi9Kc_uw1sccGcrrDjYwM5T4LpJoSiQCc1mb47Vk7kI7S5oY_X6Wv-vqDjhnyOWRGwBOFReheYGv_fMLlNr6GrPIsSVY-oh25XyCmjRJ5cME)

18. 選取「新文字文件.txt」，按鍵盤的F2按鍵，準備更改檔案名稱。

![](https://lh5.googleusercontent.com/6Fwh8LWJDb-TLRGOWxmsDhUf_-UZWn-igBFaK_OsWptwHO91do1JxPNr35gfTM0yzmOAPWgA7nM3MFyN9Ux7WVIt7LSPeF-NHbnAOJrPsYVRme1kpicFihR4vTE3-QAL1m6Nenu-)

19.將檔案名稱更改為「StaticIP.bat」，完成固定IP批次檔的設定；名稱StaticIP可自訂。

![](https://lh5.googleusercontent.com/6EVLccndToPHNONHYHRfhiMgRBWkmaLslMmfAOJDqnIlxUtoh5MSnmu4n-dVnOXvqttDxTJeFLE2yaPK8QnGwqmVVENORMB9CL_7sKk3NG4A36D6pOYlPgqZkVufqRMVf7O0RiC8)

20. 對著檔案「StaticIP.bat」按滑鼠右鍵，點選「以系統管理員身分執行」，就可以將網路連線設定為固定IP。

![](https://lh4.googleusercontent.com/xSZUDmSNqVpPmLnU-PzER1Q2eRqrLrbYzXa26OUoxVF6LagsP3WVJNwwyWbdNLzYFrtwDL3D6UDWfqrg75caQemZz1zM4DhIOy3xtzRFfoyh5TLevGlAtfO_X0KSsLPPJYoK34jt)

21. 正在將網路連線設定為固定IP，如下圖所示。

![](https://lh5.googleusercontent.com/7PJODdl-foWCRcoL9DmKgnPrrbDXWErICnnUnbsvIrGNrvX0BlWq2fIYJcXiB7YTyW07b_wQC26NQtbtFmVyW9X8wbPvlAeNGZGX0y5Rx42YMCyWhcgLdeEAfekyUYztsVB0nB2Q)