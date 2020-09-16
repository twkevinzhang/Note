## 參考 
 - [重新介紹 JavaScript](https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/A_re-introduction_to_JavaScript)


### 數字

 - 根據規格，JavaScript 數字算是「雙精確度 64 位元格式 IEEE 754 值」("double-precision 64-bit format IEEE 754 values")。這能造成一些有趣的後果。JavaScript 沒有所謂的整數，所以你在做算術的時候得小心一點，尤其是假如你習慣了 C 或 Java 的數學。小心類似下的的事情: 

        0.1 + 0.2 = 0.30000000000000004

 - 如果你不指定進位數，就有可能得到意想不到的結果: 
 
        > parseInt("010")
        8

 - JavaScript 也有特殊的值 Infinity  (無限)以及 -Infinity  (負無限)

        > 1 / 0
        Infinity
        > -1 / 0
        -Infinity

### Boolean

 - null  (空)，屬於「object」型態的一種物件，用以明言表示無數值
 - undefined  (無定義)，屬於「undefined」類型的一種物件，用以表示未初始化的值
 - 因為假如 JavaScript 遇到需要接收布林值的時候，如 if 陳述式 (見下)，便會無聲無息的進行布林轉換。有鑑於此，常常會有「真值」("true values") 與「假值」("false values") 等說法，意思是指值在布林轉換過程中會被轉成 true 或是 false。這種值也有被稱為「真的」("truthy") 或「假的」("falsy")。
 
        > Boolean("")
        false
        > Boolean(234)
        true
    
 - 雙等號運算子 (等於)會進行型態強制轉換，假如比較的資料型態不一樣，有時結果會相當有趣: 
 
        > "dog" == "dog"
        true
        > 1 == true
        true
    
   要避免型態強制轉換，要用三等號運算子 (絕對等於): 
   
        > 1 === true
        false
        > true === true
        true
        
 ### Array
 - array.length 不一定是陣列的項目數。比方說: 
 
        > var a = ["狗", "貓", "雞"];
        > a[100] = "狐";
        > a.length
        101
   別忘了－－陣列的 length 就是最高索引數加一。
   
### Function
 - arguments: 一個類似陣列的物件，內含所有遞給函式的值。以下 add 函式便可以使其接受無限量的值: 
 
        function avg() {
            var sum = 0;
            for (var i = 0, j = arguments.length; i < j; i++) {
                sum += arguments[i];
            }
            return sum / arguments.length;
        }

        > avg(2, 3, 4, 5)
        3.5
        
 如果匿名函式沒有名稱，那要怎麼樣遞迴地自我呼叫？答案是使用 arguments 物件
 
         var charsInBody = (function(elm) {
            if (elm.nodeType == 3) { // TEXT_NODE
                return elm.nodeValue.length;
            }
            var count = 0;
            for (var i = 0, child; child = elm.childNodes[i]; i++) {
                count += arguments.callee(child);
            }
            return count;
        })(document.body);
        
 由於 arguments.callee 是目前的函式，而所有的函式都是物件，你可以因此用 arguments.callee 來在多次呼叫同個函式之間儲存資料。這個函式會記得它被呼叫過多少次: 
 
        function counter() {
            if (!arguments.callee.count) {
                arguments.callee.count = 0;
            }
            return arguments.callee.count++;
        }

        > counter()
        0
        > counter()
        1
        > counter()
        2
 
 - apply(): 讓你以一陣列的參數來呼叫一個函式。
 
        > avg.apply(null, [2, 3, 4, 5])
        3.5
   第二個參數便是做為一系列參數的陣列；第一個參數稍後才會討論。重點是，函式也是物件。
   
### Object
 - Object.prototype 是一個由所有 Object 物件共享的物件。他將產生一個可供查看的關係鍊 (有個特殊的名字 prototype chain)。任何時候當我們想要使用某個不在 Object 中定義的 property 時，JavaScript 就會到 Object.prototype 裡頭尋找。因此， Object.prototype 就成為一個所有 Object 物件共用且可視的一個共享空間(物件)。這是一個提供強大工具，允許你可以在執行的任何一刻增加物件的相關函式。

        > s = new Person("Simon", "Willison");
        > s.firstNameCaps();
        TypeError on line 1: s.firstNameCaps is not a function
        
        > Person.prototype.firstNameCaps = function() {
            return this.first.toUpperCase()
        }
        > s.firstNameCaps()
        SIMON
