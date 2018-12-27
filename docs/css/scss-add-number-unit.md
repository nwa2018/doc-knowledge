# scss中如何给数值添加单位

[阅读原文](https://css-tricks.com/snippets/sass/correctly-adding-unit-number/)

`scss`语法
```
.test {
    width: 100 + px;
}
```
编译后的`css`语法
```
.test {
    width: 100px
}
```
