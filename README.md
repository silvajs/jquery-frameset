js-frameset
===========

通过div使页面自动分屏，实现与原生frameset一样的功能  
在页面加载`star-frameset.js`即可，会自动查找`$(".frameset")`进行分屏

---

### 原生的frameset使用
```
<frameset rows="25%,50%,25%">
  <frame src="/example/html/frame_a.html">
  <frame src="/example/html/frame_b.html">
  <frame src="/example/html/frame_c.html">
</frameset>
```

### js-frameset的使用方法
```
<div class="frameset" rows="25%,50%,25%">
    <div></div>
    <div></div>
    <div></div>
</div>
```

需要指定`class="frameset"`，同时需要属性`rows`或者`cols`，不能同时使用这两个属性。

`rows`和`cols`的值可以是：
- `rows="40%,60%"`：上下两部分分屏，上部分占总高的40%，下部分占总高60%
- `rows="40%,*"`：上下两屏，上部分占40%，下部分占剩下的高度
- `rows="400,*"`：上下两屏，上部分占400px，下部分占剩下的高度
- `cols="400,*,400"`：水平3屏，左部分占400px，右部分占400px，中间占剩下的宽度

### 混合使用
```
<div class='c frameset' rows="30%,20%,*">
    <div class='d'><p>hello</p></div>
    <div class='d'><p>hello</p></div>
    <div class='frameset' cols="200,*,200">
        <div class='d2'><p>hi</p></div>
        <div class='d2'><p>hi</p></div>
        <div class='d2'><p>hi</p></div>
    </div>
</div>
```
