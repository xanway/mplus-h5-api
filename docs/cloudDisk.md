# 云盘数据获取

---

<h2 id="cid_0">转存到云盘(5.1.0)</h2>

```JavaScript
//云盘-转存到个人文件
mplus.saveToCloudDisk({
    documentids: 'id1,id2...', 
    appid: '', 
    appname: '', 
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
    <th>documentids</th>
    <th>文件id列表，多个id间以”,”分割。</th>
  </tr>
  <tr>
    <th>appid</th>
    <th>h5应用id。</th>
  </tr>
  <tr>
    <th>appname</th>
    <th>h5应用名。</th>
  </tr>
  <tr>
    <th>res.errMsg</th>
    <th>错误提示。</th>
  </tr>
</table>

