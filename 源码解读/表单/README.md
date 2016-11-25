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
<p><div class="form-inline" 中的所有元素都显示在同一行，支持响应式，当屏幕小于768px时，label与input会换行</p>
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
