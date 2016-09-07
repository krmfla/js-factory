#toast.js

<b>功能描述</b>

在畫面上呈現提示訊息的效果

<b>使用</b>

1.引入toast.css樣式及toast.js模組

```javascript
<link rel="stylesheet" href="toast.css">
<script type="text/javascript" src="toast.js"></script>
```
2.語法

```javascript
var toast = new Toast("YOUR TEXT", CONFIG-OBJECT);
toast.short();
toast.long();
```
CONFIG-OBJECT
```javascript
var config = {
  "targetEl": "ELEMNET ID",  //要將提示訊息貼到哪個DOM id上 (預設為body)
  "style": "STYLE",  //可使用預設的style: "slide"或"fadeInOut"
  "inState": {  //進入效果
    "PROPERTY": "VALUE"
  },
  "outState": {  //退出效果
    "PROPERTY": "VALUE"
  },
  "speed": DURATION(millisecond),  //動畫速率
  "shortTime": DURATION(millisecond),  //自定出現時間長度(短)
  "longTime": DURATION(millisecond)  //自定出現時間長度(長)
};
```
範例
```javascript
//使用預設效果
var toast = new Toast("Welcome!");

//使用自定效果
var configData = {
  "targetEl": "main",
  "style": null,
	"inState": {
    "left": "50%",
    "bottom": "20px",
  },
  "outState": {
    "left": "-50%",
    "bottom": "-50px",
  },
  "speed": 24,
  "shortTime": 3000,
  "longTime": 6000
};
var toast = new Toast("Welcome!", configData);
```
3.DEMO:

