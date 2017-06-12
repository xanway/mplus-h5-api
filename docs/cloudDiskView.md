# 云盘界面调用

---
<h2 id="cid_0">云盘文件选择(5.1.0)</h2>

```JavaScript
//云盘-个人文件选择
mplus.selectDocsFromCloudDisk({
    success: function (res) {
    // 成功回调
    var documentArr = res.mcmDocuments;
    for(int i=0;i<documentArr.length;i++)
    {
    var id = documentArr[i].id;
    var name = documentArr[i].name; 
    var preview = documentArr[i].preview;
    var downloadflag = documentArr[i].downloadFlag;
    var createtime = documentArr[i].createtime;
    var size = documentArr[i].size;
    var documentdesc = documentArr[i].documentDesc;
    var documentcreater = documentArr[i].documentCreater;
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
    <th>mcmDocuments</th>
    <th>已选文档列表</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

###### mcmDocuments说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>id</th>
    <th>文件id</th>
  </tr>
  <tr>
  <th>name</th>
    <th>文件名</th>
  </tr>
  <tr>
    <th>preview</th>
    <th>0： 无法预览；1： 可以预览</th>
  </tr>
    <tr>
    <th>downloadFlag</th>
    <th>0： 禁止下载；1：允许下载</th>
  </tr>
  <tr>
    <th>createtime</th>
    <th>文件创建时间</th>
  </tr>
  <tr>
    <th>size</th>
    <th>文件大小，单位K</th>
  </tr>
  <tr>
    <th>documentDesc</th>
    <th>文件摘要</th>
  </tr>
  <tr>
    <th>documentCreater</th>
    <th>文件上传用户</th>
  </tr>
</table>

<h2 id="cid_0">云盘文件预览(5.1.0)</h2>

```JavaScript
//云盘-个人文件文件预览
mplus.filePreviewFromCloudDisk({
    documentid: '', 
    documentname:'', 
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
  </tr>
  <tr>
    <th>documentid</th>
    <th>文件id</th>
  </tr>
  <tr>
    <th>documentname</th>
    <th>文件名</th>
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