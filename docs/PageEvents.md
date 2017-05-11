# html5页面回调事件

---

在用户配置html5 tab页后，当切换至此html5 tab页，需提供页面激活状态回调；切换至其他页面时，要提供页面变为非激活状态回调。 html5页面加载完成，调用plusready事件

<h2 id="cid_0">页面加载完成事件</h2>

plusready事件会在页面加载完成后自动触发，表示桥接类可以使用。在此事件触发之前不能调用桥接类js，所以应该在此事件回调函数中调用页面初始化需要调用的桥接类js，而不应该在onload 事件中调用。
适配开发页面时，若需要页面加载调用桥接类，定义如下：
```html
{
        <script type="text/javascript">
        //加载完毕后触发plusready事件
        document.addEventListener("plusready",function(){
        //to do 回调事件
        },false);
        </script>
}
```
经开发发现，plusready在一些Android机型下会出现偶现的不触发现象。故Android下添加clientready事件，此事件采用和plusready不同的触发机制，会在页面加载完成后自动触发，表示桥接类可以使用。可在遇到plusready不触发时尝试使用。

定义如下：

```html
{
        <script type="text/javascript">
        //加载完毕后触发clientready事件，仅限Android
        document.addEventListener("clientready",function(){
        //to do 回调事件
        },false);
        </script>
}
```

<h2 id="cid_1">页面激活事件</h2>

onstart事件会在页面转变为激活状态时执行，可被调用多次。适配开发页面时，若需要页面加载调用桥接类，定义如下：
```html
{
        <script type="text/javascript">
        //页面激活时触发“onstart”事件
        document.addEventListener("onstart",function(){
        //to do 回调事件
        },false);
        </script>
}
```

<h2 id="cid_2">页面非激活事件</h2>

onstop事件会在页面转变为不可见触发，可被调用多次。
适配开发页面时，若需要页面不可见时调用桥接类，定义如下：

```html
{
        <script type="text/javascript">
       //页面不可见时触发“onstop”事件
        document.addEventListener("onstop",function(){
        //to do 回调事件
        },false);
        </script>
}
```