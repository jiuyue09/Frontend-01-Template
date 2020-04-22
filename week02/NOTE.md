# 1. 匹配Number

```
  // 整数
  var str1 = "123";
  var reg = /^-?\d+$/g;
  console.log(reg.test(str1));
  // 浮点数
  var str2 = "11.1234";
  var reg = /^(-?\d+)(\.\d+)?$/g;
  console.log(reg.test(str2));
  // 二进制
  var str3 = "0b00110011";
  var reg = /^0[bB][01]+$/g;
  console.log(reg.test(str3));
  // 八进制
  var str4 = "0o66117711";
  var reg = /^0[oO][0-7]+$/g;
  console.log(reg.test(str4));
  // 十六进制
  var str5 = "0xaf1e7d11";
  var reg = /^0[xX][0-9a-fA-F]+$/g;
  console.log(reg.test(str5));
  // Number
  var reg = /^-?\d+$|^(-?\d+)(\.\d+)?$|^0[bB][01]+$|^0[oO][0-7]+$|^0[xX][0-9a-fA-F]+$/g;

```


# 2. utf-8 encoding

```
function utf8Encoding(str) {
    return str.split('').map((s) => `\\u${s.charCodeAt().toString(16)}`).join('');
}
```

# 3. 匹配字符串

```
/?:[^"]|\.)*"|'(?:[^']|\.)*|^[\u4E00-\u9FA5A-Za-z0-9]+$ /
```