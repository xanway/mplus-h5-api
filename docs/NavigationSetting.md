# 导航栏(原标题栏)操作

---

在顶部导航栏，有“关闭”、“返回”和“菜单”三个按钮，可通过初始化config参数预置显示，也可以通过方法动态控制。
在webview里打开链接，除非用户设置标题栏菜单显示，否则菜单不变。
html5页面有两种，一种内嵌的，一种从新窗口打开，内嵌页面无关闭按钮，首页无返回按钮。
新窗口打开页面，默认有返回按钮，返回和关闭都可以存在。

<h2 id="cid_0">隐藏左上角关闭接口（内嵌页面无效）</h2>

```JavaScript

mplus.hideCloseButton();

```

<h2 id="cid_0">显示左上角关闭接口（内嵌页面无效）</h2>

```JavaScript

mplus.showCloseButton();

```

<h2 id="cid_0">隐藏左上角返回接口</h2>

```JavaScript

mplus.hideBackButton();

```

<h2 id="cid_0">显示左上角返回接口</h2>

```JavaScript

mplus.showBackButton();

```

<h2 id="cid_0">隐藏右上角菜单接口</h2>

```JavaScript

mplus.hideOptionButton();

```

<h2 id="cid_0">显示右上角菜单接口</h2>

```JavaScript

mplus.showOptionButton();

```

<h2 id="cid_0">是否能返回上一页接口</h2>

```JavaScript
mplus.canBack({
    success: function (res) {
        var result = res.canBack; 
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
    <th>canBack</th>
    <th>判断是否还有上一页 ,0没有,1有</th>
  </tr>
  <tr>
    <th>errMsg</th>
    <th>错误提示</th>
  </tr>
</table>

<h2 id="cid_0">返回上一页接口</h2>

```JavaScript

mplus.backPage();

```

<h2 id="cid_0">关闭当前页面（内嵌页面无效）</h2>

```JavaScript

mplus.closeWindow();

```


<h2 id="cid_0">批量隐藏功能按钮接口</h2>

```JavaScript

mplus.hideMenuItems({
    menuList: []
});


```
### 参数说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>menuList</th>
    <th>要隐藏的菜单项，所有menu项如下</th>
  </tr>
</table>

#### 所有menu项:
>•	发送给朋友: "menuItem:share:appMessage"
>
>•	分享到朋友圈: "menuItem:share:timeline"
>
>•	分享到QQ: "menuItem:share:qq"
>
>•	分享到 QQ 空间"menuItem:share:QZone"
>
>•	复制链接: "menuItem:copyUrl"
>
>•	在浏览器中打开: "menuItem:openWithBrowser"
>
>•	在Safari中打开: "menuItem:openWithSafari"

<h2 id="cid_0">批量显示功能按钮接口</h2>

```JavaScript
mplus.showMenuItems({
    menuList: [] 
});

```
### 参数说明：

<table>
  <tr>
    <th>参数</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>menuList</th>
    <th>要隐藏的菜单项</th>
  </tr>
</table>

<h2 id="cid_0">隐藏所有功能按钮接口</h2>

```JavaScript

mplus.hideAllMenuItem();

```

<h2 id="cid_0">显示所有功能按钮接口</h2>


```JavaScript

mplus.showAllMenuItem();

```


<h2 id="cid_0">隐藏头部接口</h2>

```JavaScript

mplus.hideHeader();

```

<h2 id="cid_0">显示头部接口</h2>

```JavaScript

mplus.showHeader();

```

<h2 id="cid_0">显示分享</h2>

```JavaScript

mplus.showShare();//弹出分享页面

```