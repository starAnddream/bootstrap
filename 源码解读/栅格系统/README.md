#栅格系统
* row必须包含在样式为container或者container-fluid的容器中，其中container-fluid宽度为100%。
```css
.container {
  padding-right: 15px;
  padding-left: 15px;
  margin-right: auto;
  margin-left: auto;
}
@media (min-width: 768px) {
  .container {
    width: 750px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 970px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1170px;
  }
}
```
* 通过媒体查询min-width匹配类前缀（.col-lg-$），每格宽度通过百分比控制（$/12）
```css
@media (min-width: 1200px) {
 .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
 }
 ```
* 需要注意的是bootstrap对于.col-xs-$的处理有点特殊，并没有包含在媒体查询中，所以当只声明.col-xs-$时适用于所有min-width的屏幕
<p>如果你不能理解我们看如下代码</p>
```html
<div class="col-lg-4 col-xs-6"></div>
```
```css
.col-xs-6{
position: relative;
  min-height: 1px;
  padding-right: 15px;
  padding-left: 15px;
  width: 50%;
  float:left
}
@media (min-width:1200px){
.container {
    width: 1170px;
  }
......
.col-lg-4{
 position: relative;
  min-height: 1px;
  padding-right: 15px;
  padding-left: 15px;
  width: 33.33333333%;
  float:left
}
}
```
<p>观察上面代码你会发现col-xs-6不在媒体查询里面，所以class中不包含.col-lg-4时，即便min-width大于768，也会按照col-xs-6布局</p>
* bootstrap中栅格布局是让列浮动，bootstrap中也提供了清除浮动的方法，在父元素中添加.clearfix,但我遇到了下面的问题无法解决
```html
<div class="col-xs-4 col-lg-6"></div>
......
......
<div class="col-xs-4 col-lg-6"></div>
````
<p>会出现如下问题</p>
![bug](https://github.com/starAnddream/bootstrap/blob/master/%E6%BA%90%E7%A0%81%E8%A7%A3%E8%AF%BB/images/float.png)
<p>第一个是我们想要的，但有时候我们会得到第二个，主要原因是第一个div高度过高导致,浮动会使元素尽可能的往高处浮动</p>
* 方法一：放个div在换行处
```html
<div class="clear"></div>
.clear{
clear:both
}
```
<p>这样一是不知道什么时候换行，二是改变了文档的Dom结构</p>
* 方法二：给换行的元素清除左边的浮动
```html
<div class="clear"></div>
.clear{
clear:left;
}
```
<p>我们通过js查询屏幕尺寸，如：min-width:1200px,则每隔一个添加.clear</p>
