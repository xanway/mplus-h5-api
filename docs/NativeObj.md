# NativeObj应用操作接口

---

NativeObj对象提供打开原生应用、ExMobi应用和html5应用操作

<h2 id="cid_0">应用是否安装</h2>

#### 方法名：int isInstalled(String type ,String appId)


### 参数说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>type</th>
    <th>应用类型。 
        0：原生应用；
        1：ExMobi应用；
        2：html5应用(此功能不对外)</th>
  </tr>
  <tr>
    <th>appId</th>
    <th>需要启动应用的标识(Android)或者程序入口(iOS)</th>
  </tr>
</table>

### 返回说明：

返回值： 0：应用已安装
         其他（默认-1）：应用未安装

注：
    ios 9.0以后的系统，不能判断第三方原生应用是否已安装，
    只能判断应用是否在工作台安装。

### 示例：

判断原生PushMail应用是否已安装 

```javascript
        var type = "0";
        var appId = "com.fiberhome.pushmail";
        var isInstalled = NativeObj.isInstalled(type,appId);
        if(0 == isInstalled)
        {
        //应用已安装处理
        }
        else
        {
        //应用未安装处理
        }
```

<h2 id="cid_0">启动指定应用</h2>

#### 方法名：void openApp(String type, String appId,String params)

### 参数说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>type</th>
    <th>应用类型。 
        0：原生应用；
        1：ExMobi应用；
        2：html5应用(此功能不对外)</th>
  </tr>
  <tr>
    <th>appId</th>
    <th>需要启动应用的应用ID（从管理平台获取），String类型</th>
  </tr>
  <tr>
    <th>params</th>
    <th>需要传递给应用的参数。参数如果为空，
    采用管理平台配置的应用传参；
    不为空，则采用此参数和服务器配置参数合集。</th>
  </tr>
</table>

注：
    1：parames格式为key1=value1&key2=value2

### 示例：

打开原生应用 

```javascript
        //应用标识
        var type = "0";
        var appId = "com.fiberhome.pushmail";
        //传递参数
        var params = "name=test&password=123456&token=ODRmNTk1MjYtN2I2MS00NmNkLTk0ZWMtNzgyNThiMWIyNTlm";
         //启动应用	
        NativeObj.openApp(type,appId, params);
```
<h2 id="cid_0">获取平台类型</h2>

#### 方法名：String getPhoneType()

### 返回说明：

返回值： 0：Android
         1:iOS

### 示例：

```javascript
    var phoneType = NativeObj.getPhoneType();
    if("0" == phoneType)
    {
     //Android方法调用处理
    }
    else if("1" == phoneType)
    {
    //iOS方法调用处理
    }
```

<h2 id="cid_0">获取登录账号</h2>

#### 方法名：String getUserName()


### 返回说明：

返回值： 用户登录账号

### 示例：

```javascript
    var name = NativeObj.getUserName();
```
<h2 id="cid_0">获取登录密码</h2>

#### 方法名：String getPassWord()


### 返回说明：

返回值： 用户登录密码

### 示例：

```javascript
    var password = NativeObj.getPassWord();
```

<h2 id="cid_0">获取企业id</h2>

#### 方法名：String getEcid()


### 返回说明：

返回值： 用户企业id

### 示例：

```javascript
    var ecid = NativeObj.getEcid();
```

<h2 id="cid_0">获取token</h2>

#### 方法名：String getToken()


### 返回说明：

返回值： 用户token

### 示例：

```javascript
    var token = NativeObj.getToken();
```

<h2 id="cid_0">隐藏或显示标题栏</h2>

#### 方法名：void hideHeader(boolean isHidden)


### 参数说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>isHidden</th>
    <th>true 隐藏标题栏，
        false显示标题栏</th>
  </tr>
</table>

### 示例：

```javascript
    NativeObj.hideHeader(true)
```


注：如果应用未安装，则提示用户“应用程序未安装”。