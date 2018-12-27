# 在textarea标签中格式化json字符串

[阅读原文](https://stackoverflow.com/questions/26320525/prettify-json-data-in-textarea-input)
```
function prettyPrint() {
    var ugly = document.getElementById('myTextArea').value;
    var obj = JSON.parse(ugly);
    var pretty = JSON.stringify(obj, undefined, 4);
    document.getElementById('myTextArea').value = pretty;
}
```
