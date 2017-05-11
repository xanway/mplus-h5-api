# 获取base64编码图片接口


---

```javascript
mplus.getBase64ImageFromId({
    localId: '', 
    maxLength:'', 
    pwidth:'',
    success: function (res) {
        var base64Image = res.base64Image; 
        var imgType= res.base64ImageType;
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
    <th>图片的本地ID，由chooseImage接口获得</th>
  </tr>
  <tr>
    <th>maxLength</th>
    <th>整数值，单位为KB，可不填。如果设置此值，上传的图片大小<=maxLength,如maxLength:'300'</th>
  </tr>
  <tr>
    <th>pwidth</th>
    <th>压缩之后的图片宽度，可不填。如果设置此值，必须同时设置maxLength。</th>
  </tr>
  <tr>
    <th>res.base64Image</th>
    <th>返回图片的base64编码数据，在img标签src属性填充格式：data:image/png;base64,base64编码的png图片数据  data:image/jpeg;base64,base64编码的jpeg图片数据</th>
  </tr>
  <tr>
    <th>res.base64ImageType</th>
    <th>图片类型，返回类型：”png”,”jpeg”</th>
  </tr>
 </table>