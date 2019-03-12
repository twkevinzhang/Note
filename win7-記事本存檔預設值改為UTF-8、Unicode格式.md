# win7-記事本存檔預設值改為UTF-8、Unicode格式
###### tags: `regedit` `txt` `windows` `win7` `UTF-8` `Unicode`
 參考至:[http://macrosshiking.pixnet.net/blog/post/197940064-%E8%A8%98%E4%BA%8B%E6%9C%AC%E5%AD%98%E6%AA%94%E9%A0%90%E8%A8%AD%E5%80%BC%E6%94%B9%E7%82%BAutf-8%E3%80%81unicode%E6%A0%BC%E5%BC%8F](http://macrosshiking.pixnet.net/blog/post/197940064-%E8%A8%98%E4%BA%8B%E6%9C%AC%E5%AD%98%E6%AA%94%E9%A0%90%E8%A8%AD%E5%80%BC%E6%94%B9%E7%82%BAutf-8%E3%80%81unicode%E6%A0%BC%E5%BC%8F)

#### Step 1\.

將空白記事本以UTF-8、Unicode儲存到路徑：

　`C:\Windows\ShellNew`

#### Step 2\.

開啟登陸編輯器 (regedit)

　找到`HKEY_CLASSES_ROOT\.txt\ShellNEW`

　在右方新增字串，名稱：`FileName`

　數值資料：`TXTUTF-8.txt` 或是 `TXTUnicode.txt`

在任何地方新增一個記事本，另存若編碼為 `UTF-8` 或是 `Unicode` 則成功。