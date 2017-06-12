# 其他接口

---
<h2 id="cid_0">打开第三方应用</h2>

```JavaScript
mplus.openThirdApp({
    appid: '',
    success: function (res) {
       
    },
    fail: function (res) {
        alert(res.errMsg);
    }
});

```
### 参数说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>appid</th>
    <th>android：包名；ios：程序入口</th>
  </tr>
</table>

### 返回说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

<h2 id="cid_0">获取mplus当前语言设置(5.1.3)</h2>

```JavaScript
mplus.getCurrentLanguage({
    success: function (res) {
       
       var language = res.language;
    },
    fail: function (res) {
        alert(res.errMsg);
    }
});


```

### 返回说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>language</th>
    <th>zh：中文;  en：英文</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>
