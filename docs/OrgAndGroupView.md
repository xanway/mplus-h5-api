# 界面调用

---

<h2 id="cid_0">打开联系人界面(5.1.0)</h2>

```JavaScript
mplus.openContactUI({
    success: function (res) {
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

<h2 id="cid_0">选人(5.1.0)</h2>


```JavaScript
mplus.selectMembersFromContact({
    maxCount: '', 
    success: function (res) {
    var memberArr = res.members;
	for(int i=0;i<memberArr.length;i++)
	{
	var id = memberArr[i].id; 
	var loginId= memberArr[i].loginId;
	var name = memberArr[i].name; 
	var jianpin = memberArr[i].jianpin; 
	var photoUrl = memberArr[i].photoUrl;
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
    <th>maxCount</th>
    <th>可选择人数上限，默认100，最大值500（此参数只对新联系人版本生效）</th>
  </tr>
</table>

### 返回说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>members</th>
    <th>返回成员名列表</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

###### members说明

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>id</th>
    <th>返回成员名id(member_id)</th>
  </tr>
  <tr>
    <th>loginId</th>
    <th>返回loginId</th>
  </tr>
  <tr>
    <th>name</th>
    <th>返回成员昵称</th>
  </tr>
  <tr>
    <th>jianpin</th>
    <th>姓名简拼</th>
  </tr>
  <tr>
    <th>photoUrl</th>
    <th>头像url，若为空则不存在</th>
  </tr>
</table>

<h2 id="cid_0">查看个人详情(5.1.0)</h2>

```JavaScript
mplus.openMemberDetailUI({
    memberId: '', 
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
    <th>memberId</th>
    <th>成员id</th>
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