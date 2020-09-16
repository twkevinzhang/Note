# SQL-NOT_EXISTS怎麼用
###### tags: `sql`
## 參考
  - [[blog] SQL NOT EXISTS 怎麼用？](http://frankiestudy.blogspot.com/2012/01/sql-not-exists.html)

我們先來看看 Product 資料表裡面的內容。

裡面總共有 5 筆資料。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/SQL-NOT_EXISTS怎麼用/1.png)

然後 Promotion 資料表裡面總共有 2 筆資料。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/SQL-NOT_EXISTS怎麼用/2.png)

所以我想看到的是 ProductNo 2, 4, 5 這 3 筆資料，寫法如下，請享用。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/SQL-NOT_EXISTS怎麼用/3.png)

妳問說這有甚麼用？

簡單的說，當我想把 ProductNo 2, 4, 5 這 3 筆資料塞到 Promotion 裡面去的時候就會用到這個語法啦！