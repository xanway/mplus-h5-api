# 下载图片接口

---
```JavaScript
mplus.uploadImage({
    serverId: '', 
    success: function (res) {
        var localId = res.downloadUrl; 
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
    <th>serverId</th>
    <th>需要下载的图片的服务器端ID，由uploadImage接口获得</th>
  </tr>
  <tr>
    <th>res.downloadUrl</th>
    <th>返回图片下载地址</th>
  </tr>
  <tr>
    <th>res.errMsg</th>
    <th>错误提示。</th>
  </tr>
</table>