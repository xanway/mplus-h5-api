# html5应用url传参说明

---
html5应用目前分工作台应用和html5 tab应用，url如果配置了传递的参数，需替换参数值。

如配置url：http://www.baidu.com/?username=${username}&password=${password} ，

其中 username=${username}&password=${password}的值，客户端需要进行参数替换。

客户端目前可替换值包括${username}、${password}、${token}、${ecid}、${ tokentimeout }。

新增手机端类型变量${phonetype}， 返回“0”和“1”，0表示phone，1表示为pad，

管理员在发布应用时，参数可配置成phonetype=${phonetype}。
