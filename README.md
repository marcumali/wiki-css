# Web Development Tools - HTML

[MAIN](https://github.com/marcumali/wiki) | [HTML](https://github.com/marcumali/wiki-html) | [CSS](http://www.google.com/) | [JAVASCRIPT](http://www.google.com/) | [WORDPRESS](http://www.google.com/) | [PHP](http://www.google.com/)

Guide and best practice of web development

## Scale Iframe - SASS
HTML:
```html
<div class="ratio-16-9">
	<iframe src="sourcecode"></iframe>
</div>
```

CSS:
```css
.ratio-16-9{
	height:0;
	margin-bottom: 45px;
	overflow:hidden;
	padding-bottom:56.25%;
	padding-top:30px;
  
	position:relative;
  
	iframe{
		height:100%;
		width:100%;

		left:0;
		position:absolute;
		top:0;
	}
  
}
```
