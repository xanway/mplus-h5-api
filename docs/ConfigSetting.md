#  配置参数

---
<h2 id="cid_0">config配置</h2>

```javascript

    mplus.config({
    
             accessid : '' //访问接入码，图片上传和下载接口调用前必须设置。
    });

```

<h2 id="cid_0">获取服务网关地址接口(5.2.0)</h2>

```javascript

mplus.getServiceAddress({
    success: function (res) {
        var serviceAddress = res.serviceAddress; 
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
    <th>serviceAddress</th>
    <th>应用服务网关地址</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>