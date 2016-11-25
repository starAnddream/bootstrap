# 表格
* 基础表格 在table中添加class="table"
```css
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 20px;
  border-collapse: collapse !important;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
```
* 斑马线 添加.table-striped
<p>利用css的.nth-child</p>
```css
.table-striped > tbody > tr:nth-child(odd) {
  background-color: #f9f9f9;
}
```
* 表格边框 添加.table-bordered
```css
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
```
* 高亮行 添加.table-hover
<p>当鼠标悬停时所在行高亮，通过设置tr:hover实现</p>
```css
.table-hover > tbody > tr:hover {
  background-color: #f1f1f1;
}
```
* 紧凑型表格 添加.table-condesed
```css
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
```
* 响应式表格 .table-responsive
<p>当浏览器区域小于768px时，表格底部会出现滚动条</p>
<b>这里的.table-responsive是加在.table的父元素中</b>
```css
.table-responsive {
  min-height: .01%;
  overflow-x: auto;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 15px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  }
 ```

