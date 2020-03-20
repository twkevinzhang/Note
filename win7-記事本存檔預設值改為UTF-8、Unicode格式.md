# win7-記事本存檔預設值改為UTF-8、Unicode格式
###### tags: `regedit` `txt` `windows` `win7` `UTF-8` `Unicode`
 參考至:
  - http://macrosshiking.pixnet.net/blog/post/197940064-記事本存檔預設值改為utf-8、unicode格式

#### Step 1.

將空白記事本以UTF-8、Unicode儲存到路徑：

　`C:\Windows\ShellNew`

#### Step 2.

開啟登陸編輯器 (regedit)

　找到`HKEY_CLASSES_ROOT\.txt\ShellNEW`

　在右方新增字串，名稱：`FileName`

　數值資料：`TXTUTF-8.txt` 或是 `TXTUnicode.txt`

在任何地方新增一個記事本，另存若編碼為 `UTF-8` 或是 `Unicode` 則成功。