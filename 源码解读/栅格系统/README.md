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
* 需要注意的是bootstrap对于.col-xs-$的处理有点特殊，并没有包含在媒体查询中，所以当使用.col-xs-$时适用于所有情况。 
