> JavaScript 代码的书写位置在哪里呢？这个问题，也可以理解成：引入 js 代码，有哪几种方式。

### 方式1：行内式

**代码举例**：

```javascript
<input type="button" value="点我点我" onclick="alert('千古壹号')" />
```

完整的可执行代码如下：

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Document</title>
    </head>
    <body>
        <input type="button" value="点我点我" onclick="alert('方式1')" />
    </body>
</html>

```


### 方式2、内嵌式

我们可以在html 页面的 `<body>` 标签里放入`<script type=”text/javascript”></script>`标签对儿，并在`<script>`里书写JavaScript 代码：

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	<script type="text/javascript">
		alert('方式2');
		console.log('方式2');
	</script>
</body>
</html>
```

### 方式3：引入外部的 JS 文件

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	<!-- 引入外部的 js 文件 -->
	<script src="tool.js"></script>
</body>
</html>
```

> 这里的话要注意跟css 的引入有些区别，css 的话，是使用link 然后 使用href 进行引入

## JS一些简单的语法规则

学习程序，是有规律可循的，程序会有有相同的部分，这些部分就是一种规定，不能更改，我们成为：语法。

（1）JavaScript对换行、缩进、空格不敏感。每一条语句以分号结尾。

也就是说：

代码一：

```html
<script type="text/javascript">
	alert("白云");
	alert("高兴");
</script>
```

等价于代码二：

```html
<script type="text/javascript">
	alert("白云");alert("高兴");
</script>
```

备注：每一条语句末尾要加上分号，虽然分号不是必须加的，如果不写分号，浏览器会自动添加，但是会消耗一些系统资源。

（2）所有的符号，都是英语的。比如**括号**、引号、分号。

如果你用的是搜狗拼音，**建议不要用shift切换中英文**（可以在搜狗软件里进行设置），不然很容易输入中文的分号；建议用ctrl+space切换中英文输入法。

（3）严格区分大小写。

## 注释

我们不要把 HTML、CSS、JavaScript三者的注释格式搞混淆了。

### HTML 的注释

```html
<!-- 我是注释  -->
```

### CSS的注释

```html
<style type="text/css">

	/*
		我是注释
	*/

	p{
		font-weight: bold;
		font-style: italic;
		color: red;
	}

</style>
```

注意：CSS只有`/*  */`这种注释，没有`//`这种注释。而且注释要写在`<style>`标签里面才算生效哦。

### JavaScript 的注释

单行注释：

```
// 我是注释
```

多行注释：

```
/*
	多行注释1
	多行注释2
*/
```

补充：VS Code中，单行注释的快捷键是「Ctrl + /」，多行注释的默认快捷键是「Alt + Shift + A」。

当然，如果你觉得多行注释的默认快捷键不方便，我们还可以修改默认快捷键。操作如下：

VS Code --> 首选项 --> 键盘快捷方式 --> 查找“注释”这两个字 --> 将原来的快捷键修改为「Ctrl + Shift + /」。

## Javascript 输入输出语句

### 弹出警告框：alert语句

我们要学习的第一个语句，就是alert语句。

代码举例如下：

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Document</title>
    </head>
    <body>
        <script>
            alert('千古壹号');
        </script>
    </body>
</html>

```

**alert**（英文翻译为“警报”）的用途：**弹出“警告框”**。

### 控制台输出：console.log("")

`console.log("")`表示在控制台中输出。console表示“控制台”，log表示“输出”。

在Chrome浏览器中，按F12即可打开控制台，选择「console」栏，即可看到打印的内容。

**总结**：alert() 主要用来显示消息给用户，console.log() 用来给程序员自己调试用的。

### 弹出输入框：prompt()语句

`prompt()`就是专门用来弹出能够让用户输入的对话框。用得少，测试的时候偶尔会用。

JS代码如下：

```javascript
var a = prompt("请随便输入点什么东西吧");
console.log(a);
```

**prompt()语句中，用户不管输入什么内容，都是字符串。**

**alert()和prompt()的区别：**

- alert() 可以直接使用。

- prompt() 会返回用户输入的内容。我们可以用一个变量，来接收用户输入的内容。
