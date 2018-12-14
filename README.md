# Web Development Tools - CSS

[MARCUMALI](https://marcumali.github.io) | 
[MAIN](https://github.com/marcumali/wiki) | [HTML](https://github.com/marcumali/wiki-html) | [CSS](https://github.com/marcumali/wiki-css) | [JAVASCRIPT](https://github.com/marcumali/wiki-javascript) | [WORDPRESS](https://github.com/marcumali/wiki-wordpress) | [PHP](https://github.com/marcumali/wiki-php)

Guide and best practice of web development

## CSS

* try to avoid page specific css since it's not a modular way of working don't nestle more than 2 levels unless:
* `:pseudo. @content-mixins` or media query (then aim keep it under 4)
* mobile first since it prevents CSS reset on mobile
* `.js-classes` (preferably) or `#js-id` for javascript functions connected to the DOM
* Use `http://b64.io/` for svgs and save us from http requests and horrible svg sprites.

## Good selector intent / low specifity in SCSS, avoid

* There are some exceptions to these rules but 98% of the time they should apply.
* IDs e.g. `#my-page`
* Types e.g. `header`
* Descendants e.g. `ul li`
* Selector nestle e.g. `.block ul li a`
* Qualified selectorns e.g. `ul.a`
* Long selectors e.g. `.home .header ul.primary-nav .primary-nav-link`
* Universals

## Syntax

* be specific or generic
* do not use camelCase on selectors, use lower-case and hyphen-delimited syntax
* row break after each selector { and }
* every rule on it's own line
* space after property:
* space between selector and {
* space between selector combinators e.g. `.selector` ~ `.selector`
* include a semicolon at the end of the last declaration in a declaration block.
* use simple quotation for 'strings'
* properties with 0-value should not have a unit e.g. `margin: 0 10px 0 0;`
* include a space after each comma in comma-separated property values e.g. `rgba(0, 0, 0, .5)`
* media queries nestled in class
* hover-state within media-query since there's no reliable way to check for touchscreen
* long, comma-separated property values - such as collections of gradients or shadows can be arranged across multiple lines in an effort to improve readability e.g.
* the order of properties in a selector:
	- `@extend`
	- `@include` without inner `@content`
	- properties, alphabetic order
	- `@include` with inner `@content`
	- nested rule sets
* vendor prefix order:
	- `-moz-`
	- `-webkit-`
	- `no vendor`

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
