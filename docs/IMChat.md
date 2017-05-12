# IM聊天接口

---
<h2 id="cid_0">获取IM类型</h2>

```JavaScript

mplus.getImType({
    success: function (res) { 
        // 发送成功回调
        var imType = res.imType;
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
    <th>imType</th>
    <th>0：烽火IM；1：容联云</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

<h2 id="cid_0">发送消息给用户或群组（容联云）</h2>

```JavaScript

mplus.sendMessage({
    imaccount: '', 
    message: '',
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
    <th>imaccount</th>
    <th>im用户或群组账号</th>
  </tr>
  <tr>
    <th>message</th>
    <th>发送内容</th>
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

<h2 id="cid_0">发送消息给用户</h2>

烽火IM和容联云通用
```JavaScript
mplus.sendChatMessage({
    imaccount: '', 
    message: '',
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
    <th>imaccount</th>
    <th>im用户账号</th>
  </tr>
  <tr>
    <th>message</th>
    <th>发送内容</th>
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

<h2 id="cid_0">发送消息给群组</h2>

烽火IM和容联云通用
```JavaScript
mplus.sendGroupMessage({
    imaccount: '', 
    message: '',
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
    <th>imaccount</th>
    <th>im群组账号</th>
  </tr>
  <tr>
    <th>message</th>
    <th>发送内容</th>
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

<h2 id="cid_0">显示聊天界面（容联云）</h2>

```JavaScript
mplus.showMessage({
    imaccount: '', 
    name: '',
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
    <th>imaccount</th>
    <th>im用户账号</th>
  </tr>
  <tr>
    <th>name</th>
    <th>用户名称</th>
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

<h2 id="cid_0">显示单个聊天界面</h2>

烽火IM和容联云通用
```JavaScript
mplus.showChatMessage({
    imaccount: '', 
    name: '',
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
    <th>imaccount</th>
    <th>im用户账号</th>
  </tr>
  <tr>
    <th>name</th>
    <th>用户名称</th>
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

<h2 id="cid_0">获取IM类型</h2>

```JavaScript

//烽火IM和容联云通用
mplus.showGroupMessage({
    imaccount: '',
    name: '',
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
    <th>imaccount</th>
    <th>im群组账号</th>
  </tr>
  <tr>
    <th>name</th>
    <th>群名</th>
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