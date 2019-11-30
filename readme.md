# Paint CSS

---

## Table of Contents
+ [Overview](../master/readme.md#overview)
+ [Setup](../master/readme.md#setup)
+ [Getting Started with Paint](../master/readme.md#getting-started-with-paint)
+ [Classes](../master/readme.md#classes)
+ [Usage Examples](../master/readme.md#usage-examples)


## Overview
Paint is a simple, lightweight, modular CSS framework that allows you rapidly layout and style responsive websites without 
having to write much additional CSS.

[Check out the example site, built entirely with Paint and regular HTML](https://ahl389.github.io/paint-css-framework/)

## Setup
Head to the `src/SCSS` directory and grab the `paint.scss file`, along with the `reset.scss` and `variables.scss` files, and save them in your project's CSS directory. `paint.scss` file is designed to be your primary stylesheet, but doesn't have to be. If want an additional stylesheet, just dont forget to import `paint.scss`.

## Getting Started with Paint
Paint is simple enough that getting acquainted and starting to build your website can happen in minutes.

The idea is that Paint lets you 'paint' on styles to your HTML elements by applying a series of basic,
easy to remember classes.  For this to work, your HTML must be structured using Paint's basic building
blocks: section, container, and module.

#### Section

Sections are page-wide elements that you use to organize the major parts of a webpage in a vertical manner.
Each section must have the class 'banner'.  

```html
<section class = "banner" id = "banner-your-id">
</section>
```

Banner elements don't get `painted`! But many times you may want to use an `id` or special `class` to add background styling or custom padding sizes.

#### Container

Within each section block, you will have immediately have a `div` element with the class `container`.  The default container element is set to 90% of the page width, is centered, and has a max-width of 1200px.  

```html
<section class = "banner" id = "banner-your-id">
	<div class = "container">
	</div>
</section>
```

Container elements can be painted with the following types of classes (see [classes](#classes) section):
+ [Fonts & Text](#fonts-and-text) (Note: These will be applied to the entire contents of the container)
+ [Content Alignment within Containers](#container-alignment)

#### Module

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

## Classes

Paint's classes govern module width, alignment, margin, padding, along with font size,
weight, and decoration.  There are also stock classes for images and buttons, and very 
basic styles for heading, paragraph, and a tags.

Typical order of class application is as follows:
width, panel, padding, margin, alignment, font styles

```html
<div class = "module per80 panel padding-small margin-top margin-bottom">
	<h3 class = "bold">H3 Heading</h3>
	<p class = "margin-top italic">Content</p>
</div>
```


Available classes include:

##### Building Blocks
+ .banner
+ .container
+ .container-extender
+ .module


##### General

+ .button
+ .panel
+ .panel.highlight


##### Fonts and Text
+ .mini (.6em)
+ .small (.8em)
+ .medium (1em)
+ .large (1.25em)
+ .xl (1.75em)
+ .x2 (2.5em)
+ .x3 (3.5em)
+ .x4 (4em)
+ .uppercase
+ .lowercase
+ .capitalize
+ .bold
+ .italic


##### Module Width
Each of these classes indicate a percentage width.  Adding a padding class to any module will not alter its outer width.

+ .p10
+ .p15
+ .p20
+ .p25
+ .p30
+ .p33 (33.33%)
+ .p35
+ .p40
+ .p45
+ .p50
+ .p55
+ .p60
+ .p65
+ .p70
+ .p75
+ .p80
+ .p85
+ .p90
+ .p95
+ .p100


##### Module Width (Tablet)
+ .p10-tab
+ .p20-tab
+ .p25-tab
+ .p30-tab
+ .p33-tab (33.33%)
+ .p40-tab
+ .p50-tab
+ .p60-tab
+ .p70-tab
+ .p75-tab
+ .p80-tab
+ .p90-tab
+ .p100-tab


##### Module Width (Mobile)
+ .p10-mob
+ .p20-mob
+ .p25-mob
+ .p30-mob
+ .p33-mob (33.33%)
+ .p40-mob
+ .p50-mob
+ .p60-mob
+ .p70-mob
+ .p75-mob
+ .p80-mob
+ .p90-mob
+ .p100-mob


##### Module Order (Tablet)
+ .tab-order-1
+ .tab-order-2
+ .tab-order-3
+ .tab-order-4
+ .tab-order-5
+ .tab-order-6
+ .tab-order-7
+ .tab-order-8
+ .tab-order-9


##### Module Order (Mobile)
+ .mob-order-1
+ .mob-order-2
+ .mob-order-3
+ .mob-order-4
+ .mob-order-5
+ .mob-order-6
+ .mob-order-7
+ .mob-order-8
+ .mob-order-9


##### Text Alignment
+ .text-left (default)
+ .text-center
+ .text-right


##### To Align All Modules Within a Container (Apply to container)<a name="container-alignment">
+ .align-left 
+ .align-center 
+ .align-right 
+ .align-top
+ .align-middle 
+ .align-bottom 
+ .align-stretch 


##### To Align Individual Modules (Apply to module)
+ .self-align-top
+ .self-align-middle 
+ .self-align-bottom
+ .self-align-left
+ .self-align-right


##### Padding - 4 Sides
+ .padding-mini (8px)
+ .padding-small (15px)
+ .padding-medium (30px)
+ .padding-large (50px)


##### Padding - 1 Side 
+ .padding-top-mini (8px)
+ .padding-top-small (15px)
+ .padding-top-medium (30px)
+ .padding-top-large (50px)
+ .padding-right-mini(-small, -medium, -large)
+ .padding-bottom-mini(-small, -medium, -large)
+ .padding-left-mini(-small, -medium, -large)


##### Margin - 1 side (All 30px)
+ .margin-top
+ .margin-right
+ .margin-bottom
+ .margin-left
+ .margin-center

## Usage Examples

#### One column, half-page wide, centered
```html
<section class = "banner" id = "banner-three-columns">
	<div class = "container align-center">
		<div class = "module per50">
			<!-- content -->
		</div>
	</div>
</section>
```


#### Three column grid

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

#### Sub-columns/Nested Columns

```html
<section class = "banner" id = "banner-sub-column">
	<div class = "container align-center">
		<div class = "module per50">
			<!-- content -->
		</div>
		<div class = "module per50">
			<div class = "module-container"
				<div class = "module per40">
					<!-- content -->
				</div>
				<div class = "module per60">
					<!-- content -->
				</div>
			</div>
		</div>
	</div>
</section>
```

#### Panel

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

#### Full width / edge extended panel

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

#### Text styles

```html
<div class = "module per100">
	<h2 class = "margin-bottom uppercase">Section Title</h2>
	<p class = "italic bold large">Section sub-title</p> 
</div>
````
