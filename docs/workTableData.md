# 数据操作接口

---
<h2 id="cid_0">获取已安装应用列表(5.0.4)</h2>

```JavaScript
mplus.getInstalledAppList({
    apptype: '',
    success: function (res) { 
        var installedAppArr = res.installedAppArr; 
        for(int i=0;i< installedAppArr.length;i++)
        {
        var appid = installedAppArr[i].appid; 
        Var apptype = installedAppArr[i].apptype; 
        var name = installedAppArr[i].name; 
        var size = installedAppArr[i].size;
        var version = installedAppArr[i].version;
        }
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
    <th>apptype</th>
    <th>应用类型: 0：原生应用；1：ExMobi应用；2：html5应用；3：全部</th>
  </tr>
</table>

### 返回说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
    <tr>
    <th>installedAppArr</th>
    <th>返回已安装应用列表</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

###### installedAppArr说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>appid</th>
    <th>应用id</th>
  </tr>
  <tr>
  <th>apptype</th>
    <th>应用类型</th>
  </tr>
  <tr>
    <th>name</th>
    <th>应用名</th>
  </tr>
  <tr>
    <th>size</th>
    <th>应用大小</th>
  </tr>
  <tr>
    <th>version</th>
    <th>版本号</th>
  </tr>
</table>

<h2 id="cid_0">应用安装检测</h2>

参照NativeObj应用操作接口

int isInstalled(String type ,String appId)

<h2 id="cid_0">启动应用</h2>

参照NativeObj应用操作接口

void openApp(String type, String appId,String params)

<h2 id="cid_0">应用安装或更新检测(5.4.1)</h2>

```JavaScript
mplus.isNeedInstallOrUpdate({
    apptype: '',
    appid: '',
    success: function (res) { 
       var result = res.status;
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
    <th>apptype</th>
    <th>应用类型: 0：原生应用；1：ExMobi/Sprite应用；2：html5应用；</th>
  </tr>    
  <tr>
    <th>appid</th>
    <th>应用id</th>
  </tr>
</table>

### 返回说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>status</th>
    <th>0：已安装且为最新版本；1：未安装；2：检测有新版本</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

<h2 id="cid_0">应用安装更新(5.4.1)</h2>

```JavaScript
//安装过程为工作台逻辑处理，安装成功后会给提示
mplus.installApp({
    apptype: '',
    appid: '',
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
    <th>apptype</th>
    <th>应用类型: 0：原生应用；1：ExMobi/Sprite应用；2：html5应用；</th>
  </tr>    
  <tr>
    <th>appid</th>
    <th>应用id</th>
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
