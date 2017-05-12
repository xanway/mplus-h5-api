# 圈子数据操作

---
<h2 id="cid_0">获取登录用户已关注圈子列表(5.1.0)</h2>

```JavaScript
mplus.getFollowWorkCircle({
    success: function (res) {
        var circleArr = res.circles;
        for(int i=0;i<circleArr.length;i++)
        {
        var id = circleArr[i].id;
        var type = circleArr[i].type; 
        var name = circleArr[i].name; 
        var cover = circleArr[i].cover; 
        var creator = circleArr[i].creator;
        var remark = circleArr[i].remark;
        }
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
    <th>circles</th>
    <th>圈子列表</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

###### circles说明

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>id</th>
    <th>圈子id</th>
  </tr>
  <tr>
    <th>type</th>
    <th>1-普通圈子，2-默认圈子</th>
  </tr>
    <tr>
    <th>name</th>
    <th>圈子名称</th>
  </tr>
  <tr>
    <th>cover</th>
    <th>封面</th>
  </tr>
    <tr>
    <th>creator</th>
    <th>创建者</th>
  </tr>
  <tr>
    <th>remark</th>
    <th>圈子说明</th>
  </tr>
</table>

<h2 id="cid_0">分享h5应用到圈子(5.1.0)</h2>

```JavaScript
mplus.shareWorkCircle({
    comment: '',
    title: '',
    desc: '',
    appname: '',
    appid: '',
    imgUrl: '',
    link: '',
    id: '',
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
    <th>comment</th>
    <th>用户评论</th>
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
  <tr>
    <th>id</th>
    <th>圈子id</th>
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