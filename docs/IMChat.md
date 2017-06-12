# IM聊天接口

---
<h2 id="cid_0">获取IM类型</h2>

```JavaScript

mplus.getImType({
    success: function (res) { 
        
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

<h2 id="cid_0">显示群组聊天界面</h2>

```JavaScript

//烽火IM和容联云通用
mplus.showGroupMessage({
    imaccount: '',
    name: '',
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


<h2 id="cid_0">分享h5应用到IM(5.2.0)</h2>

```JavaScript

mplus.shareIMUI({
    title: '',
    desc: '',
    appname: '',
    appid: '',
    imgUrl: '',
    link: '',
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
    <th>title</th>
    <th>分享标题</th>
  </tr>
    <tr>
    <th>desc</th>
    <th>分享描述</th>
  </tr>
  <tr>
    <th>appname</th>
    <th>分享应用名</th>
  </tr>
    <tr>
    <th>appid</th>
    <th>分享应用id</th>
  </tr>
  <tr>
    <th>imgUrl</th>
    <th>分享图标，见imgUrl链接格式定义</th>
  </tr>
    <tr>
    <th>link</th>
    <th>分享链接，见link链接格式</th>
  </tr>
</table>


##### imgUrl链接格式：

>1）以http、https开头，表示网络图片
>
>2）以local开头，格式local:imgname，为客户端打包内置图片资源。
例：local:icon.png
>
>3）以app_local开头，格式app_local:apptype:appid:imgpath，为企业应用图片资源。例：app_local:apptype:appid:/img/icon.png
其中apptype为应用类型，目前固定为4，表示html5应用
appid为应用id
>

##### link链接格式
>其中apptype为填应用类型，Exmobi应用填1，原生应用填2，html5应用填4。
>
>当apptype为2时，appid为原型应用ID，格式为androidappid##iosappid，客户端使用##截取自行操作系统的应用ID，并且使用自行操作系统的apptype请求服务器做应用打开。
>
>当apptpye为1或者2时，系统将请求格式中？后续参数作为启动传参传递给应用。例如：app_scheme://apptype:appid/param?type=xxx&file=xxx
>
>当apptpye为4时，系统将param后续参数作为应用url打开，打开的ip、端口、协议使用应用发布时的数据。例如：app_scheme://apptype:appid/param/index?type=xxx&file=xxx
>
