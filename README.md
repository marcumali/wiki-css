# Web Development Tools - CSS

[MARCUMALI](https://marcumali.github.io) | 
[MAIN](https://github.com/marcumali/wiki) | [HTML](https://github.com/marcumali/wiki-html) | [CSS](https://github.com/marcumali/wiki-css) | [JAVASCRIPT](https://github.com/marcumali/wiki-javascript) | [WORDPRESS](https://github.com/marcumali/wiki-wordpress) | [PHP](https://github.com/marcumali/wiki-php)

Guide and best practice of web development

## 1. Scale Iframe
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
	overflow: hidden;
	padding-bottom: 56.25%;
	padding-top: 30px;
  
	position: relative;
  
	iframe{
		height: 100%;
		width: 100%;

		left: 0;
		position: absolute;
		top: 0;
	}
  
}
```
