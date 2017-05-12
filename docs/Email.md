# 启动系统邮件

---

IOS会启动到发邮件页面，可返回到邮件列表页面

```JavaScript

mplus.startEmail({
    success: function (res) {
    	// 成功回调
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
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>
