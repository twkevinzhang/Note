# Python“Non-ASCII character 'xe5' in file”
###### tags:`Python` `error` `coding`

參考至:
 - https://blog.csdn.net/geekmanong/article/details/50514984

### error:
> SyntaxError: Non-ASCII character '\xe5' in file kNN.py on line 24, but no encoding declared; see

### 解決方法:
在開頭加上` # -*- coding: UTF-8 -*-`