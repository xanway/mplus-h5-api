# 摇一摇

---
开启监听后，当用户摇一摇返回成功回调后，此次监听自动结束，如果想再次使用摇一摇功能，需再次开启监听

<h2 id="cid_0">开启监听(5.1.0)</h2>

```JavaScript

mplus.watchShake({
    success: function (res) {
     
    },
    fail: function (res) {
        alert(res.errMsg);
    }
});

```
### 返回说明

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

<h2 id="cid_0">清除监听(5.1.0)</h2>

```JavaScript

mplus.clearShake({
    success: function (res) {
        
    },
    fail: function (res) {
        alert(res.errMsg);
    }
});

```
### 返回说明

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