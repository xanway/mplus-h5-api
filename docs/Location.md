# 地理位置接口

---
<h2 id="cid_0">选择当前地理位置接口</h2>

```JavaScript

mplus.chooseLocation({
    range:'1500',
    success: function (res) {
        var latitude = res.latitude; 
        var longitude = res.longitude; 
        var name = res.name; 
        var address = res.address; 
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
    <th>range</th>
    <th>地图显示范围，单位米，-1，不做控制</th>
  </tr>
</table>

### 返回说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>latitude</th>
    <th>纬度，浮点数，范围为90 ~ -90</th>
  </tr>
    <tr>
    <th>longitude</th>
    <th>经度，浮点数，范围为180 ~ -180。</th>
  </tr>
    <tr>
    <th>name</th>
    <th>位置名</th>
  </tr>
    <tr>
    <th>address</th>
    <th>地址详情说明</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>


<h2 id="cid_0">使用百度地图查看位置接口</h2>

```JavaScript

mplus.openLocation({
    latitude: 0, 
    longitude: 0,
    name: '',
    address: '',
    scale: 1,
});


```
### 参数说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>latitude</th>
    <th>纬度，浮点数，范围为90 ~ -90</th>
  </tr>
    <tr>
    <th>longitude</th>
    <th>经度，浮点数，范围为180 ~ -180。</th>
  </tr>
    <tr>
    <th>name</th>
    <th>位置名</th>
  </tr>
    <tr>
    <th>address</th>
    <th>地址详情说明</th>
  </tr>
  <tr>
    <th>scale</th>
    <th>地图缩放级别,整型值,范围从1~28。默认为最大</th>
  </tr>
</table>

<h2 id="cid_0">获取当前地理位置接口</h2>

```JavaScript

mplus.getLocation({
    success: function (res) {
        var latitude = res.latitude;
        var longitude = res.longitude;
        var speed = res.speed; 
        var address = res.address; 
        var province = res.province; 
        var city = res.city;
        var district = res.district;
        var street= res.street;
        var streetNumber = res.streetNumber;
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
    <th>latitude</th>
    <th>纬度，浮点数，范围为90 ~ -90</th>
  </tr>
    <tr>
    <th>longitude</th>
    <th>经度，浮点数，范围为180 ~ -180。</th>
  </tr>
    <tr>
    <th>speed</th>
    <th>速度，以米/每秒计</th>
  </tr>
  <tr>
    <th>address</th>
    <th>地址详情说明</th>
  </tr>
  <tr>
    <th>province</th>
    <th>省名</th>
  </tr>
  <tr>
    <th>city</th>
    <th>城市名</th>
  </tr>
    <tr>
    <th>district</th>
    <th>县区名</th>
  </tr>
    <tr>
    <th>street</th>
    <th>街道名</th>
  </tr>
  <tr>
    <th>streetNumber</th>
    <th>街道门牌号</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>