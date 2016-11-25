# 表单
* 基本实例 .form-group
```html
<div class="container">
		<h1>test</h1>
		<div class="form-group">
			<label for="userName">用户名</label>
			<input type="text" class="form-control" name="userName" id="userName" placeholder="请输入用户名"/>
		</div>
		<div class="form-group">
			<label for="passWord">密码</label>
			<input type="text" name="passWord" class="form-control" id="passWord" placeholder="请输入密码"/>
		</div>
	</div>
```
```css
.form-group {
  margin-bottom: 15px;
}
.input-sm,
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 3px;
}
```
#### 内联表单  .form-inline
<b>.form-inline是加在form-group的父元素上的</b>
<p>div class="form-inline"中的所有元素都显示在同一行，支持响应式，当屏幕小于768px时，label与input会换行</p>
```html
<div class="form-inline">
			
		<div class="form-group">
			<label for="userName">用户名</label>
			<input type="text" class="form-control" name="userName" id="userName" placeholder="请输入用户名"/>
		</div>
		<div class="form-group">
			<label for="passWord">密码</label>
			<input type="text" name="passWord" class="form-control" id="passWord" placeholder="请输入密码"/>
		</div>
		</div>
	</div>
  ```
  ```css
  @media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  ```
* 水平表单方法一：.form-horizontal配合col-type-$栅格
<p>label与input同行</p>
<b>类名也是加在form-group的父元素上</b>
```css
.form-horizontal .form-group {
  margin-right: -15px;
  margin-left: -15px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    padding-top: 7px;
    margin-bottom: 0;
    text-align: right;
  }
}
```
* 水平表单方法二：自定义样式
```css
.horizontal .form-control{
		display:inline-block;
		width:auto;
		vertical-align:middle;
	}
```
* 输入框
#### 下拉框 .form-control
```html
<select class="form-control">    //单选框
	<option></option>
	...
	...
	<option></option>
</select>
<select class="form-control" multiple="multiple">    //多选框
	<option></option>
	...
	...
	<option></option>
</select>




