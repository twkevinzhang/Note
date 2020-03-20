# SQL-NOT EXISTS 怎麼用？
###### tags: `sql`
 參考至:
  - http://frankiestudy.blogspot.com/2012/01/sql-not-exists.html

我們先來看看 Product 資料表裡面的內容。

裡面總共有 5 筆資料。

![](https://lh5.googleusercontent.com/sxocvOJK2aSEW9aHAft70Ivi-2cmpsPmQB0V1cf2beNXegJhjZXcu9p3gcs74awSQBE5WS21E1pmYSwitQq4oVdtOfHbCKpSQ-HZMqGoYVbn5f3bYxcaBanKgMUkQ1ja_Ccq-9oC)

然後 Promotion 資料表裡面總共有 2 筆資料。

![](https://lh4.googleusercontent.com/Dp6nzeZkFhkXyO80o8qDMu62WU3yJphHpTJLZ05ByyaNLSxFZLDz65PHcPdFjYc16b9S6b2XI_nl-VDHvbfzaDl-78Z942kjXtn8T4w_G4qiMpWR2vcRrSl4f_ads4OPNWJoKJhC)

所以我想看到的是 ProductNo 2, 4, 5 這 3 筆資料，寫法如下，請享用。

![](https://lh6.googleusercontent.com/l0TZf-ASdIIbZdyqtXvphwITS5__m9F6hvU8yhblNJtGj_JfQrpxv5iKAEcNmav6FD3NE71VIXgSiXQTU9096x3N5-7YdBHlXlo5HkVaX5vypPc8OUcvXM_ICSgoGkllHepGEE31)

妳問說這有甚麼用？

簡單的說，當我想把 ProductNo 2, 4, 5 這 3 筆資料塞到 Promotion 裡面去的時候就會用到這個語法啦！