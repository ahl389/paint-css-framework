#Paint CSS

---

##Table of Contents
+ [Overview](../Paint-CSS-Framework/blob/master/readme.md#overview)
+ [Setup](../Paint-CSS-Framework/blob/master/readme.md#setup)
+ [Getting Started with Paint](../Paint-CSS-Framework/blob/master/readme.md#getting-started-with-paint)
+ [Classes](../Paint-CSS-Framework/blob/master/readme.md#classes)
+ [Usage Examples](../Paint-CSS-Framework/blob/master/readme.md#usage-examples)


##Overview
Paint is a simple, lightweight, modular CSS framework that allows you rapidly layout and style responsive websites without 
having to write much additional CSS.

##Setup
Grab the source paint.css file and save in your project's CSS directory. This file is designed to be your primary stylesheet.

##Getting Started with Paint
Paint is simple enough that getting acquainted and starting to build your website can happen in minutes.

The idea is that Paint lets you 'paint' on styles to your HTML elements by applying a series of basic,
easy to remember classes.  For this to work, your HTML must be structured using Paint's basic building
blocks: section, container, and module.

####Section

Sections are page-wide elements that you use to organize the major parts of a webpage in a vertical manner.
Each section must have the class 'banner'.  

```html
<section class = "banner" id = "banner-your-id">
</section>
```

####Container

Within each section block, you will have a container element.  The default container element is set to 90%
of the page width, is centered, and has a max-width of 1200px.  

```html
<section class = "banner" id = "banner-your-id">
	<div class = "container">
	</div>
</section>
```

####Module

Module elements are created inside container elements.  Modules are your more basic content block/element.
They will automatically flow from left to right. At the very least, you assign each module a width class.

```html
<section class = "banner" id = "banner-your-id">
	<div class = "container">
		<div class = "module per50">
		</div>
	</div>
</section>
```

##Classes

Paint's classes govern module width, alignment, margin, padding, along with font size,
weight, and decoration.  There are also stock classes for images and buttons, and very 
basic styles for heading, paragraph, and a tags.

Typical order of class application is as follows:
width, panel, padding, margin, alignment, font styles

```html
<div class = "module per25 panel padding-small align-top">
	<!-- content here -->
</div>
```

```html
<div class = "module per80 margin-top margin-bottom">
	<h3 class = "bold">H3 Heading</h3>
	<p class = "margin-top italic">Content</p>
</div>
```


Available classes include:

#####Building Blocks
+ .banner
+ .container
+ .container-extender
+ .container-inner
+ .module


#####General

+ .button
+ .panel
+ .panel.highlight
+ .clear-fix (special use case)
+ .image-bleed


#####Fonts & Text
+ .mini
+ .small
+ .medium
+ .large
+ .x2
+ .x3
+ .uppercase
+ .lowercase
+ .bold
+ .italic


#####Module Width
Each of these classes indicate a percentage width.  Adding a padding class to any module will not alter its outer width.

+ .per10
+ .per20
+ .per25
+ .per30
+ .per33 (33+ .3333% width)
+ .per40
+ .per50
+ .per60
+ .per70
+ .per75
+ .per80
+ .per90
+ .per100


#####Text Alignment
+ .align-left (default)
+ .align-center
+ .align-right


#####Module Vertical Alignment
+ .align-top
+ .align-middle (default)
+ .align-bottom


#####Padding - 4 Sides
+ .padding-mini (8px)
+ .padding-small (15px)
+ .padding-medium (30px)
+ .padding-large (50px)


#####Padding - 1 Side (All 15px)
+ .padding-top
+ .padding-right
+ .padding-bottom
+ .padding-left


#####Margin - 1 side (All 30px)
+ .margin-top
+ .margin-right
+ .margin-bottom
+ .margin-left
+ .margin-center

##Usage Examples

####One column, half-page wide, centered
```html
<section class = "banner" id = "banner-three-columns">
	<div class = "container align-center">
		<div class = "module per50">
			<!-- content -->
		</div>
	</div>
</section>
```


####Three column grid

```html
<section class = "banner" id = "banner-three-columns">
	<div class = "container align-center">
		<div class = "module per33">
			<!-- content -->
		</div>
		<div class = "module per33">
			<!-- content -->
		</div>
		<div class = "module per33">
			<!-- content -->
		</div>
	</div>
</section>
```

####Sub-columns

```html
<section class = "banner" id = "banner-sub-column">
	<div class = "container align-center">
		<div class = "module per50">
			<!-- content -->
		</div>
		<div class = "module per50">
			<div class = "module per40">
				<!-- content -->
			</div>
			<div class = "module per60">
				<!-- content -->
			</div>
		</div>
	</div>
</section>
```

####Panel

```html
<section class = "banner" id = "banner-panel">
	<div class = "container align-center">
		<div class = "module per80 padding-right">
			<!-- content -->
		</div>
		<div class = "module per20 padding-left">
			<div class = "module per100 panel padding-medium">
				<!-- content -->
			</div>
		</div>
	</div>
</section>
```

####Full width / edge extended panel

Notice the slightly different structure and container elements.
The panel class can be applied to both module elements for a split screen
color effect.

```html
<section class = "banner" id = "banner-special-case">
	<div class = "container-extended align-center">
		<div class = "module per50 panel align-right padding-medium">
			<div class = "container-inner align-center">
				<!-- content -->
			</div>
		</div>
		<div class = "module per50 align-left padding-medium">
			<div class = "container-inner align-center">
				<!-- content -->
			</div>
		</div>
	</div>
</section>
```

####Text styles

```html
<div class = "module per100">
	<h2 class = "margin-bottom uppercase">Section Title</h2>
	<p class = "italic bold large">Section sub-title</p> 
</div>
````
