# 快速切換網路連線的IP
###### tags: `batch` `網路` `IP` `windows` `windows 7`

## 參考
 - [[xuite] 快速切換Windows網路連線的IP](http://blog.xuite.net/yh96301/blog/240237360-快速切換Windows網路連線的IP)

## 步驟
只要使用Windows內建的命令「netsh」建立自動執行批次檔，就可以快速切換網路連線的IP，詳細操作說明如下: 

1. 在工作列「網路的捷徑圖示」按滑鼠右鍵，點選「開啟網路和共用中心」。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/1.png)

2. 點選「變更介面卡設定」。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/2.png)

3. 記住你的有線網路的名稱，如下圖所示名稱為「區域連線」〈不同的電腦，名稱可能不一樣〉。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/3.png)

4. 在桌面按滑鼠右鍵，點選「新增文字文件」。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/4.png)

5. 直接按鍵盤的「Enter」鍵，完成「新文字文件」的新增。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/5.png)

6. 對著「新文字文件.txt」連續按兩下滑鼠左鍵，開啟文件。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/6.png)

7. 在文件輸入下列兩行文字，將網路設定為DHCP，其中「區域連線」為電腦有線網路的名稱。輸入的文字如下: 

```
netsh interface ipv4 set address "區域連線" source=dhcp
netsh interface ipv4 set dnsserver "區域連線" source=dhcp
```

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/7.png)

8. 點選「檔案儲存檔案」，儲存文字文件。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/8.png)

9. 選取「新文字文件.txt」，按鍵盤的F2按鍵，準備更改檔案名稱。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/9.png)

10. 將檔案名稱更改為「DHCP.bat」，完成DHCP批次檔的設定；名稱DHCP可自訂。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/10.png)

11. 對著檔案「DHCP.bat」按滑鼠右鍵，點選「以系統管理員身分執行」，就可以將網路連線設定為DHCP。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/11.png)

12. 正在將網路連線設定為DHCP，如下圖所示。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/12.png)

13. 在桌面按滑鼠右鍵，點選「新增文字文件」。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/13.png)

14. 直接按鍵盤的「Enter」鍵，完成「新文字文件」的新增。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/14.png)

15. 對著「新文字文件.txt」連續按兩下滑鼠左鍵，開啟文件。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/15.png)

16. 在文件輸入下列三行文字，將網路設定為固定IP，其中「區域連線」為電腦有線網路的名稱，192.168.1.38為連線IP，255.255.255.0為子網路遮罩，192.168.1.1為預設閘道，8.8.8.8為慣用DNS伺服器，8.8.4.4為其他DNS伺服器；上述的資料只做為說明用途，你必須填入自己的IP、DNS等相關數字。輸入的文字如下: 

```
netsh interface ipv4 set address "區域連線" static 192.168.1.38 255.255.255.0 192.168.1.1
netsh interface ipv4 set dnsserver "區域連線" static 8.8.8.8 primary
netsh interface ipv4 add dns "區域連線" 8.8.4.4
```

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/16.png)

17. 點選「檔案儲存檔案」

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/17.png)

18. 選取「新文字文件.txt」，按鍵盤的F2按鍵，準備更改檔案名稱。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/18.png)

19. 將檔案名稱更改為「StaticIP.bat」，完成固定IP批次檔的設定；名稱StaticIP可自訂。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/19.png)

20. 對著檔案「StaticIP.bat」按滑鼠右鍵，點選「以系統管理員身分執行」，就可以將網路連線設定為固定IP。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/20.png)

21. 正在將網路連線設定為固定IP，如下圖所示。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/快速切換網路連線的IP/21.png)