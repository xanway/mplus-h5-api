# 机构和群组获取接口

---
<h2 id="cid_0">获取机构名</h2>

```JavaScript
mplus.getOrgName({
    success: function (res) {
        var orgName = res.orgName;
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
    <th>orgName</th>
    <th>返回机构名称</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

<h2 id="cid_1">获取子部门</h2>

```JavaScript

mplus.getOrgGroups({
    groupId:'',
    success: function (res) {
        	var orgGroupArr = res.orgGroups; 
	        for(int i=0;i< orgGroupArr.length;i++)
            {
            var id = orgGroupArr[i].id;
            var name = orgGroupArr[i].name; 
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
    <th>groupId</th>
    <th>指定的部门id，根节点为-1</th>
  </tr>
</table>

### 返回说明：
<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>orgGroups</th>
    <th>返回子部门数组</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

###### orgGroups说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>id</th>
    <th>返回子部门id</th>
  </tr>
  <tr>
    <th>name</th>
    <th>返回子部门名称</th>
  </tr>
</table>

<h2 id="cid_2">获取部门直属成员</h2>


```JavaScript
mplus.getOrgMembers({
    groupId:'',
    success: function (res) {
        var orgMemberArr = res.orgMembers;
        for(int i=0;i<orgMemberArr.length;i++)
        {
            var id = orgMemberArr[i].id; 
            var loginId= orgMemberArr[i].loginId; 
            var name = orgMemberArr[i].name; 
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
    <th>groupId</th>
    <th>指定的部门id，根节点为-1</th>
  </tr>
</table>

### 返回说明：
<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>orgMembers</th>
    <th>返回部门成员数组</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

###### orgMembers说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>id</th>
    <th>返回部门成员名id</th>
  </tr>
  <tr>
    <th>loginId</th>
    <th>返回loginId</th>
  </tr>
  <tr>
    <th>name</th>
    <th>返回部门成员昵称</th>
  </tr>
</table>

<h2 id="cid_2">获取部门直属成员和子部门</h2>

```Javascript

mplus.getOrgGroupsAndMembers({
    groupId:'',
    success: function (res) {
    	var orgGroupArr = res.orgGroups; 
        var orgMemberArr = res.orgMembers; 
    	for(int i=0;i< orgGroupArr.length;i++)
    	{
            var id = orgGroupArr[i].id;
            var name = orgGroupArr[i].name;
    	}
    	for(int i=0;i<orgMemberArr.length;i++)
    	{
            var id = orgMemberArr[i].id;
            var loginId= orgMemberArr[i].loginId;
            var name = orgMemberArr[i].name;
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
    <th>groupId</th>
    <th>指定的部门id，根节点为-1</th>
  </tr>
  <tr>
    <th>res.orgGroups</th>
    <th>返回子部门数组</th>
  </tr>
  <tr>
    <th>res.orgMembers</th>
    <th>返回部门成员数组</th>
  </tr>
  <tr>
    <th>res.errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

### 返回说明：
<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>orgGroups</th>
    <th>返回子部门数组</th>
  </tr>
  <tr>
    <th>orgMembers</th>
    <th>返回部门成员数组</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

###### orgGroups说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>id</th>
    <th>返回子部门id</th>
  </tr>
  <tr>
    <th>name</th>
    <th>返回子部门名称</th>
  </tr>
</table>

###### orgMembers说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>id</th>
    <th>返回部门成员名id</th>
  </tr>
  <tr>
    <th>loginId</th>
    <th>返回loginId</th>
  </tr>
  <tr>
    <th>name</th>
    <th>返回部门成员昵称</th>
  </tr>
</table>

<h2 id="cid_3">根据关键字搜索成员</h2>


```JavaScript
mplus.searchOrgMembers({
    condition: '',
    fieldcode: '',
    fieldvalue: '',
    limit: '',
    from: '', 
    success: function (res) {
    	var orgMemberArr = res.orgMembers;
    	for(int i=0;i<orgMemberArr.length;i++)
    	{
    	    var id = orgMemberArr[i].id; 
    	    var loginId= orgMemberArr[i].loginId; 
    	    var name = orgMemberArr[i].name; 
    	    var departmentId = orgMemberArr[i].departmentId; 
    	    var departmentName = orgMemberArr[i].departmentName; 
    	    var imAccount = orgMemberArr[i].imAccount;
    	    var phone = orgMemberArr[i].phone; 
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
    <th>condition</th>
    <th>模糊查询条件</th>
  </tr>
  <tr>
    <th>fieldcode</th>
    <th>自定义字段的编码，数据从getOrgCustomFields中获取</th>
  </tr>
  <tr>
    <th>fieldvalue</th>
    <th>自定义字段key对应的数据，需要查询的条件</th>
  </tr>
  <tr>
    <th>limit</th>
    <th>分页查询每页返回数据条数，如20</th>
  </tr>
  <tr>
    <th>from</th>
    <th>分页查询从第几页开始，如0，第一页以此类推</th>
  </tr>
  <tr>
    <th>res.orgMembers</th>
    <th>返回部门成员数组</th>
  </tr>
  <tr>
    <th>res.errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

### 返回说明：
<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>orgMembers</th>
    <th>返回部门成员数组</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

###### orgMembers说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>id</th>
    <th>返回部门成员名id</th>
  </tr>
  <tr>
    <th>loginId</th>
    <th>返回loginId</th>
  </tr>
  <tr>
    <th>name</th>
    <th>返回部门成员昵称</th>
  </tr>
  <tr>
    <th>departmentId</th>
    <th>返回部门id</th>
  </tr>
  <tr>
    <th>departmentName</th>
    <th>返回部门名称</th>
  </tr>
  <tr>
    <th>imAccount</th>
    <th>返回部门成员IM账号</th>
  </tr>
  <tr>
    <th>phone</th>
    <th>返回部门成员手机号码</th>
  </tr>
</table>

<h2 id="cid_4">根据成员id获取成员详细信息</h2>

id可由mplus.getOrgMembers中id获取


```JavaScript
mplus.getMemberDetails({
    memberId: '',
    //loginid: '',
    success: function (res) {
    	var phones = res.phones;
    	var imAccount = res.imAccount;
    	var name = res.name; 
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
    <th>成员id（与loginid只能选择一个参数）</th>
  </tr>
  <tr>
    <th>loginid</th>
    <th>登录id（与memberid只能选择一个参数）</th>
  </tr>
</table>

### 返回说明：
<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>phones</th>
    <th>成员电话号码数组</th>
  </tr>
  <tr>
    <th>imAccount</th>
    <th>IM账号（5.1.0版本添加）</th>
  </tr>
  <tr>
    <th>name</th>
    <th>昵称（5.1.0版本添加）</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

<h2 id="cid_5">获取群组</h2>


```JavaScript
mplus.getUserGroups({
success: function (res) {
	var userGroupArr = res.userGroups;
    for(int i=0;i< userGroupArr.length;i++)
	{
	    var id = userGroupArr[i].id;
	    var name= userGroupArr[i].name;
	} 
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
    <th>userGroups</th>
    <th>返回用户群组数组</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示。</th>
  </tr>
</table>

###### userGroupArr说明：
<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>id</th>
    <th>返回群组id</th>
  </tr>
  <tr>
    <th>name</th>
    <th>返回群组名称</th>
  </tr>
</table>

<h2 id="cid_6">获取群组成员</h2>

```JavaScript
mplus.getUserGroupMembers({
    groupId:'',
    success: function (res) {
        var userMemberArr = res.userGroupMembers;
        for(int i=0;i< userMemberArr.length;i++)
        {
            var id = userMemberArr[i].id;
            var name= userMemberArr[i].name;
            var loginId= userMemberArr[i].loginId; 
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
    <th>groupId</th>
    <th>指定的群组id</th>
  </tr>
</table>

### 参数说明：
<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>userGroupMembers</th>
    <th>返回群组成员数组</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

###### userGroupMembers说明：
<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>id</th>
    <th>返回群组成员id</th>
  </tr>
  <tr>
    <th>name</th>
    <th>返回群组成员名称</th>
  </tr>
    <tr>
    <th>loginId</th>
    <th>返回loginId</th>
  </tr>
</table>

<h2 id="cid_7">获取当前用户所在部门id</h2>

```JavaScript
mplus.getUserGroupId({
    success: function (res) {
        var groupId = res.groupId;
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
    <th>groupId</th>
    <th>用户所在部门id</th>
  </tr>
  <tr>
    <th>res.errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

<h2 id="cid_8">获取当前用户所在部门全路径id</h2>


```JavaScript
mplus.getUserGroupFullId({
    success: function (res) {
        var groupFullId = res.groupFullId;
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
    <th>groupFullId</th>
    <th>groupFullId以@分隔，从上到下，最底层为直属部门id，
    如&lt;groupfullid&gt;b1f00858-0b99-1212-910d-c75ssa7eb16f@ec5    ea37e-e5fb-4cfc-1212-00d24d750d2b@19494f45-46af-1212-a329-39b886ggc6a3@10aaa8c3-2437-1122-8e01-baffce320927&lt;/groupfullid&gt;</th>
  </tr>
  <tr>
    <th>res.errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

<h2 id="cid_10">获取当前用户姓名</h2>


```JavaScript
mplus.getUserName({
    success: function (res) {
        var userName = res.userName;
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
    <th>userName</th>
    <th>当前用户姓名</th>
  </tr>
  <tr>
    <th>res.errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

<h2 id="cid_10">获取当前机构个人信息扩展字段</h2>


```JavaScript
mplus.getOrgCustomFields({
    success: function (res) {
        var orgCustomArrs= res.orgCustomFields;
        for(int i=0;i<orgCustomArrs.length;i++)
        {
            var fieldname = orgCustomArrs[i].fieldname; 
            var fieldcode = orgCustomArrs[i].fieldcode; 
            var fieldattr= orgCustomArrs[i].fieldattr; //0:其他，1：手机，2：固定电话，3：邮箱
            var fieldpro= orgCustomArrs[i].fieldpro; //0：普通属性，1：权限属性
            var valuetype= orgCustomArrs[i].valuetype; //0:输入框，1：选择
            var defaultvalue= orgCustomArrs[i].defaultvalue; //可能为选择的数据，例如：[男、女]
        }
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
    <th>orgCustomFields</th>
    <th>当前机构扩展字段对象数组</th>
  </tr>
  <tr>
    <th>res.errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

###### userGroupMembers说明：
<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>fieldname</th>
    <th>字段名称</th>
  </tr>
  <tr>
    <th>fieldcode</th>
    <th>字段编码</th>
  </tr>
    <tr>
    <th>fieldattr</th>
    <th>0:其他，1：手机，2：固定电话，3：邮箱</th>
  </tr>
  <tr>
    <th>fieldpro</th>
    <th>0：普通属性，1：权限属性</th>
  </tr>
  <tr>
    <th>valuetype</th>
    <th>0:输入框，1：选择</th>
  </tr>
    <tr>
    <th>defaultvalue</th>
    <th>可能为选择的数据，例如：[男、女]</th>
  </tr>
</table>
