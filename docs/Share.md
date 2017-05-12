# 分享接口

---
<h2 id="cid_0">获取“分享到朋友圈”按钮点击状态及自定义分享内容接口</h2>

```JavaScript

mplus.onMenuShareTimeline({
    title: '',
    link: '', 
    imgUrl: '', 
    success: function (res) { 
        // 用户确认分享后执行的回调函数
    },
    cancel: function (res) { 
        // 用户取消分享后执行的回调函数
    }
});

```
### 参数说明

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
    <th>link</th>
    <th>分享链接</th>
  </tr>
  <tr>
    <th>imgUrl</th>
    <th>分享图标</th>
  </tr>
</table>

<h2 id="cid_0">获取“分享到朋友”按钮点击状态及自定义分享内容接口</h2>

```JavaScript

mplus.onMenuShareAppMessage({
    title: '',
    desc: '', 
    link: '',
    imgUrl: '',
    type: '',
    dataUrl: '',
    success: function (res) { 
        // 用户确认分享后执行的回调函数
    },
    cancel: function (res) { 
        // 用户取消分享后执行的回调函数
    }
});


```
### 参数说明

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
    <th>link</th>
    <th>分享链接</th>
  </tr>
  <tr>
    <th>imgUrl</th>
    <th>分享图标</th>
  </tr>
  <tr>
    <th>type</th>
    <th>分享类型,music、video或link，不填默认为link</th>
  </tr>
  <tr>
    <th>dataUrl</th>
    <th>如果type是music或video，则要提供数据链接，默认为空</th>
  </tr>
</table>

<h2 id="cid_0">获取“分享到QQ”按钮点击状态及自定义分享内容接口</h2>

```JavaScript

mplus.onMenuShareQQ({
    title: '',
    desc: '', 
    link: '',
    imgUrl: '',
    success: function (res) { 
        // 用户确认分享后执行的回调函数
    },
    cancel: function (res) { 
        // 用户取消分享后执行的回调函数
    }
});


```
### 参数说明

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
    <th>link</th>
    <th>分享链接</th>
  </tr>
  <tr>
    <th>imgUrl</th>
    <th>分享图标</th>
  </tr>
</table>

<h2 id="cid_0">获取“分享到QQ空间”按钮点击状态及自定义分享内容接口</h2>

```JavaScript

mplus.onMenuShareQZone({
    title: '',
    desc: '', 
    link: '',
    imgUrl: '',
    success: function (res) { 
        // 用户确认分享后执行的回调函数
    },
    cancel: function (res) { 
        // 用户取消分享后执行的回调函数
    }
});


```
### 参数说明

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
    <th>link</th>
    <th>分享链接</th>
  </tr>
  <tr>
    <th>imgUrl</th>
    <th>分享图标</th>
  </tr>
</table>