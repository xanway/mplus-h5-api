# 返回键控制

---
注：IOS 5.1.0版本开始支持，Android已支持

<h2 id="cid_0">设置是否监听返回键接口</h2>

android包括硬件返回键和导航栏返回按钮；ios为导航栏返回按钮

```JavaScript

mplus.setBackListener({
    active: '' 
});

```
### 参数说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>active</th>
    <th>是否要监听返回键 0 否; 1是 。如若监听返回键，则ARK不再处理返回键事件，如需ARK处理，需解除监听</th>
  </tr>
</table>

<h2 id="cid_0">返回键事件</h2>

```html

<script type="text/javascript">
document.addEventListener("backpressed",function(){
//to do 回调事件
},false);
</script>

```
