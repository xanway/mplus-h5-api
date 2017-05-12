# 设备信息

---
<h2 id="cid_0">获取网络状态接口</h2>

```JavaScript

mplus.getNetworkType({
    success: function (res) {
        var networkType = res.networkType; 
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
    <th>networkType</th>
    <th>返回网络类型2g，3g，4g，wifi</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示。</th>
  </tr>
</table>

<h2 id="cid_0">获取设备类型接口</h2>

```JavaScript

mplus.getDeviceType({
    success: function (res) {
        var deviceType = res.deviceType; 
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
    <th>deviceType</th>
    <th>phone 或 pad</th>
  </tr>
</table>

<h2 id="cid_0">获取设备信息详情(5.0.4)</h2>

```JavaScript
mplus.getDeviceInfo({
    success: function (res) {
        var deviceModel = res.deviceModel;  
        var deviceOS = res.deviceOS;  
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
    <th>deviceModel</th>
    <th>设备型号</th>
  </tr>
  <tr>
    <th>deviceOS</th>
    <th>操作系统</th>
  </tr>
</table>

<h2 id="cid_0">获取屏幕分辨率(5.1.0)</h2>


```JavaScript
mplus.getDeviceResolution({
    success: function (res) {
        var screenW= res.width;  
        var screenH = res.height;  
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
    <th>width</th>
    <th>屏幕宽度</th>
  </tr>
  <tr>
    <th>height</th>
    <th>屏幕高度</th>
  </tr>
</table>