# NativeObj应用操作接口

---

NativeObj对象提供打开原生应用、ExMobi应用和html5应用操作

<table border="1">
  <tr>
    <th>方法名</th>
    <th>描述</th>
    <th>示例</th>
  </tr>
  <tr>
    <td>int isInstalled(String type ,String appId)</td>
    <td>判断应用是否已安装
参数：
type：打开应用类型。 
0：原生应用；
1：ExMobi应用；
2：html5应用(此功能不对外)
appId：需要启动应用的标识(Android)或者程序入口(iOS)

返回值：0：应用已安装
        其他（默认-1）：应用未安装

注：ios 9.0以后的系统，不能判断第三方原生应用是否已安装，只能判断应用是否在工作台安装。
</td>
<td>判断原生PushMail应用是否已安装 
//应用标识
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
</td>
  <tr>
    <th>void openApp(String type, String appId,String params)</th>
    <th>启动指定应用
参数： 
type：打开应用类型。 
0：原生应用；
1：ExMobi应用；
2：html5应用(此功能不对外)
appId：需要启动应用的应用ID（从管理平台获取），String类型
params：需要传递给应用的参数。参数如果为空，采用管理平台配置的应用传参；不为空，则采用此参数和服务器配置参数合集。
返回值：无
注：
1：parames格式为key1=value1&key2=value2
</th>
    <th>打开原生应用 
//应用标识
var type = "0";
var appId = "com.fiberhome.pushmail";
//传递参数
var params = "name=test&password=123456&token=ODRmNTk1MjYtN2I2MS00NmNkLTk0ZWMtNzgyNThiMWIyNTlm";
//启动应用				NativeObj.openApp(type,appId, params);
</th>
  </tr>
  </tr>
</table>