# 拍照或从手机相册中选图接口

---
```javascript
        mplus.chooseImage({
        max: ''
        sourceType: ['album', 'camera'], 
        showOption:1,// 0或1， 默认为1，sourceType只有一项（相册或相机）时，选择框是否显示。0：直接弹出相册或者相机页面；1：弹出选择框
        success: function (res) {
         var localIds = res.localIds; // 返回选定照片的本地ID列表，localId作为上传图片接口使用
        },
	    fail: function (res) {
         alert(res.errMsg);
        }
});

```

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
   <tr>
    <th>max</th>
    <th>最多选择图片张数，正整数，范围1~9，最多只能选择9张图片，超出默认为9</th>
  </tr>
    <tr>
    <th>sourceType</th>
    <th>可以指定来源是相册还是相机，默认二者都有</th>
  </tr>
   <tr>
    <th>showOption</th>
    <th> 0或1， 默认为1，sourceType只有一项（相册或相机）时，选择框是否显示。0：直接弹出相册或者相机页面；1：弹出选择框</th>
  </tr>
    <tr>
    <th>localIds</th>
    <th> 返回选定照片的本地ID列表，localId作为上传图片接口使用</th>
  </tr>
  </table>
  
  
> max：最多选择图片张数，正整数，范围1~9，最多只能选择9张图片，超出默认为9；
>
>sourceType：可以指定来源是相册还是相机，默认二者都有；  
>
>showOption：0或1，默认为1，sourceType只有一项（相册或相机）时，选择框是否显示。
0：直接弹出相册或者相机页面；
1：弹出选择框。
>
>localIds：返回选定照片的本地ID列表，localId作为上传图片接口使用。
>