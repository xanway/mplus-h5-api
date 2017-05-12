# 浏览器接口

---
<h2 id="cid_0">url在浏览器中打开</h2>

```JavaScript
mplus.openWithBrowser({
    url: '', 
    success: function (res) { 
       // 发送成功回调
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
    <th>url</th>
    <th>url地址</th>
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

<h2 id="cid_0">设置webview控件是否可调试(Android)</h2>

```JavaScript
mplus.setDebug({
    isDebug: 0,
    success: function (res) { 
       // 发送成功回调
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
    <th>isDebug</th>
    <th>是否可调试。0：默认，不可调试；1：可调式</th>
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

<h2 id="cid_0">清除webview浏览器控件缓存(5.0.5)</h2>

注：此接口不能清楚cookie数据，只适合开发时调用，不要在发布应用中使用

```JavaScript

mplus.clearWebViewCache({
    success: function (res) { 
       // 发送成功回调
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
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>