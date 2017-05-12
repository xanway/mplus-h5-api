# 工作台界面调用

---
<h2 id="cid_0">打开应用详情页面</h2>

```JavaScript
mplus.openAppDetail({
    appid: '', 
    apptype: '',
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
    <th>appid</th>
    <th>应用id</th>
  </tr>
  <tr>
    <th>apptype</th>
    <th>应用类型: 0：原生应用；1：ExMobi应用；2：html5应用</th>
  </tr>
  <tr>
    <th>res.errMsg</th>
    <th>错误提示。</th>
  </tr>
</table>

<h2 id="cid_0">工作台页面唤起(5.1.0)</h2>

```JavaScript
mplus.openWorktableUI({
    success: function (res) {
    	// 成功回调
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
  <tr>
    <th>res.errMsg</th>
    <th>错误提示。</th>
  </tr>
</table>