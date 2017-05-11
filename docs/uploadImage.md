# 上传图片接口

---

```JavaScript
mplus.uploadImage({
    localId: '', 
    maxLength:'',
    isShowProgressTips: 1, 
    pwidth:'',
    success: function (res) {
        var serverId = res.serverId; 
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
    <th>localId</th>
    <th>需要上传的图片的本地ID，由chooseImage接口获得</th>
  </tr>
  <tr>
    <th>maxLength</th>
    <th>整数值，单位为KB，可不填。如果设置此值，上传的图片大小<=maxLength,如maxLength:'300'</th>
  </tr>
  <tr>
    <th>isShowProgressTips</th>
    <th>0或1， 默认为1，显示进度提示（显示上传中）</th>
  </tr>
  <tr>
    <th>pwidth</th>
    <th>压缩之后的图片宽度，可不填。如果设置此值，必须同时设置maxLength。</th>
  </tr>
  <tr>
    <th>res.serverId</th>
    <th>返回图片的服务器端ID。</th>
  </tr>
  <tr>
    <th>res.errMsg</th>
    <th>上传失败的错误提示。</th>
  </tr>
</table>