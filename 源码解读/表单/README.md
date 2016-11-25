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
<h5>下拉框 .form-control</h5>
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
```
```css
.form-control {
  display: block;
  width: 100%;
  height: 34px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 4px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, .075);
          box-shadow: inset 0 1px 1px rgba(0, 0, 0, .075);
  -webkit-transition: border-color ease-in-out .15s, -webkit-box-shadow ease-in-out .15s;
       -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
          transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, .6);
          box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, .6);
}
```
* 文本域 .form-control rows="$"
```html
<textarea class="form-control" rows="3"></textarea>
```
* 多选框和单选框 
```html
<div class="radio">
		<label class="checkbox">
			<input type="radio" name=""><label>男</label>
			<input type="radio" name=""><label>女</label>
		</label>
		</div>
```
```css
input[type="checkbox"],
input[type="radio"] {
  -webkit-box-sizing: border-box;
     -moz-box-sizing: border-box;
          box-sizing: border-box;
  padding: 0;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-top: 4px \9;
  margin-left: -20px;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  vertical-align: middle;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
```
<p>如果需要radio和checkbox在同一行，可以使用.radio-inline .checkbox-inline</p>
<b>对于radio,name值必须一样，否则可以多选</b>
* 表单属性
##### 表单禁用
<p>disabled="disabled"</p>
##### 表单是否选中
checked="true/false"
* 验证样式
<pre>
.has-warning 黄
.has-error   红
.has-success 绿
</pre>
<b>在父元素上添加类名</b>
```css
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, .075);
          box-shadow: inset 0 1px 1px rgba(0, 0, 0, .075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, .075), 0 0 6px #ce8483;
          box-shadow: inset 0 1px 1px rgba(0, 0, 0, .075), 0 0 6px #ce8483;
}
```
* 图标提示 .has-feedback
<p>在input后面添加一个span</p>
<b>类名添加的位置与has-warning一样</b>
```css
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 42.5px;
}
```
```html
<div class="horizontal">
			
			<div class="form-group has-warning form-group-lg">
				<label for="userName" class="control-label">用户名</label>
				<input type="text" class="form-control" focus name="userName" id="userName" placeholder="请输入用户名"/>
				<span class="glyphicon glyphicon glyphicon-ok sr-only" aria-hidden="true"></span>
			</div>
			</div>
```
<p>自定义css</p>
```css
.horizontal .form-control{
		display:inline-block;
		width:auto;
		vertical-align:middle;
	}
```
* 按钮 .btn
<p>按钮风格</p>
<pre>
.btn-default
.btn-success
.btn-primary
.btn-info
.btn-danger
.btn-link
.btn-warning
</pre>
<p>按钮大小</p>
<pre>
.btn-lg
.btn-sm
.btn-xs
</pre>
<p>至于如何实现，应该很简单，这里就不赘述了</p>
<h5> 块状按钮  .btn-block</h5>
<p>百分之百填充父元素</p>
```css
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
```
<h5>激活和禁用</h5>
<pre>
.disabled  | disabled="disabled"
.active
.focus
.hover
</pre>













































