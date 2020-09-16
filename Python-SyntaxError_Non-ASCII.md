# Python-SyntaxError_Non-ASCII
###### tags:`Python` `Compile Error` `encoding`

## 參考
 - [[csdn] Python“Non-ASCII character 'xe5' in file”报错问题](https://blog.csdn.net/geekmanong/article/details/50514984)

## 錯誤描述:
> SyntaxError: Non-ASCII character '\xe5' in file kNN.py on line 24, but no encoding declared;

## 原因: 
Python默认是以ASCII作为编码方式的，如果在自己的Python源码中包含了中文（或者其他非英语系的语言），此时即使你把自己编写的Python源文件以UTF-8格式保存了，但实际上，这依然是不行的。

### 解決:
 - 在開頭加上` # -*- coding: UTF-8 -*-`