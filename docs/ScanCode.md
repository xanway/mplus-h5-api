# 扫一扫

---
<h2 id="cid_0">调起扫一扫接口</h2>

```JavaScript
mplus.scanQRCode({
    success: function (res) {
        var result = res.resultStr;
	},
	fail: function (res) {
        alert(res.errMsg);
	}
});


```
### 返回说明

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
    <tr>
    <th>resultStr</th>
    <th>扫码返回的结果</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示。</th>
  </tr>
</table>