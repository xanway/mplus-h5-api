# 拨打电话

---

```JavaScript
mplus.callPhone({
    phones: [], 
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
    <th>phones</th>
    <th>号码数组</th>
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