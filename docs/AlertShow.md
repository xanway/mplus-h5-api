# 弹窗接口

---

<h2 id="cid_0">日期选择器(5.1.0)</h2>

```JavaScript
mplus.datePicker({
    format: 'yyyy-MM-dd',
    value: '2017-03-23', 
    success: function (res) {
      	// 成功回调
	var date = res.value;
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
    <th>format</th>
    <th>目前format只支持yyyy-MM-dd</th>
  </tr>
  <tr>
    <th>value</th>
    <th>默认显示日期</th>
  </tr>
</table>

### 返回说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>value</th>
    <th>返回选择时间,格式"2017-03-23"</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

<h2 id="cid_0">时间选择器(5.1.0)</h2>

```JavaScript
mplus.timePicker({
    format: 'HH:mm',
    value: '16:00',
    success: function (res) {
      	// 成功回调
	var date = res.value;
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
    <th>format</th>
    <th>目前format只支持HH:mm</th>
  </tr>
  <tr>
    <th>value</th>
    <th>默认显示时间</th>
  </tr>
</table>

### 返回说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>value</th>
    <th>返回选择时间,格式"18:00"</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>
