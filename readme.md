# Paint CSS

---

## Table of Contents
+ [Overview](../master/readme.md#overview)
+ [Setup](../master/readme.md#setup)
+ [Getting Started with Paint](../master/readme.md#getting-started-with-paint)
+ [Classes](../master/readme.md#classes)
+ [Usage Examples](../master/readme.md#usage-examples)


## Overview
Paint is a simple, lightweight, modular CSS framework that allows you rapidly layout and style responsive websites without having to write much additional CSS.

[Check out the example site, built entirely with Paint and regular HTML](https://ahl389.github.io/paint-css-framework/)

## Setup

[SCSS](#scss) / [CSS](#css)
### SCSS

Head to the `src/SCSS` directory in this repo and grab the following files:

- `paint.scss`
- `reset.scss`
- `variables.scss`
- `custom.scss`

`paint.scss` is the primary file with the majority of Paint's relevant code. 

`reset.scss` contains all the basic CSS resets so can Paint can start with its own clean slate. 

`variables.scss` defines the basic set of variables used throughout Paint. It's common that you might want to modify these values to best suit your needs, or add new variables in this file to support your custom CSS.

`custom.scss` is an additional empty file preloaded into `paint.scss` and is the appropriate location for all custom CSS you want to layer on top of Paint. 

### CSS


Save these files to your project's CSS directory. `paint.scss` file is designed to be your primary stylesheet, but doesn't have to be. If want an additional stylesheet, just dont forget to import `paint.scss`. Don't want to use `.scss`? No problem, make a copy of the `.css` file. The only downside to using the `.css` file is the loss of variables to make wholesale modifications/customizations to the base Paint styles.

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

Module elements are created inside container elements.  Modules are your basic content block/element.
They will automatically flow from left to right. In most use cases, you will paint them with a `width` class, but it's not required. If you don't paint them with a `width` class, then they assume their natural width. THis is useful when creating navigation bars, for example.

```html
<section class = "banner" id = "banner-your-id">
	<div class = "container">
		<div class = "module per50">
		</div>
	</div>
</section>
```

Modules can be assigned any or all of the following [class types](#classes):
+ [Fonts & Text](#fonts-and-text) (Note: These will be applied to the entire contents of the module)
+ [Individual Module Alignment within Container](#module-alignment)
+ [Module Width](#width) (Including Module Width on Tablet and Mobile)
+ [Module Order](#order) (Including Module Order on Tablet and Mobile)
+ [Padding](#padding)
+ [Margin](#margin)


## Classes

Paint's classes govern module width, alignment, margin, padding, along with font size,
weight, and decoration.  There are also stock classes for images and buttons, and very 
basic styles for heading, paragraph, and a tags.

Typical order of class application is as follows:
width, panel, padding, margin, alignment, font styles

```html
<div class = "module per80 panel padding-small margin-right margin-bottom">
	<h3 class = "bold">H3 Heading</h3>
	<p class = "margin-right italic">Content</p>
</div>
```


Available classes include:

#### Building Blocks
+ .banner
+ .container
+ .container-extender
+ .module


#### General

+ .button
+ .panel
+ .panel.highlight


#### Fonts and Text
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
+ .text-left (default)
+ .text-center
+ .text-right


#### Module Width<a name="width"></a>
Each of these classes indicate a percentage width (the `w` in front of each number is for `width`) relative to its parent container or module.  Adding a padding class to any module will not alter its outer width.

##### Desktop

+ .w10
+ .w15
+ .w20
+ .w25
+ .w30
+ .w33 (33.33%)
+ .w35
+ .w40
+ .w45
+ .w50
+ .w55
+ .w60
+ .w65
+ .w70
+ .w75
+ .w80
+ .w85
+ .w90
+ .w95
+ .w100


##### Tablet
+ .w10-tab
+ .w20-tab
+ .w25-tab
+ .w30-tab
+ .w33-tab (33.33%)
+ .w40-tab
+ .w50-tab
+ .w60-tab
+ .w70-tab
+ .w75-tab
+ .w80-tab
+ .w90-tab
+ .w100-tab


##### Mobile
+ .w10-mob
+ .w20-mob
+ .w25-mob
+ .w30-mob
+ .w33-mob (33.33%)
+ .w40-mob
+ .w50-mob
+ .w60-mob
+ .w70-mob
+ .w75-mob
+ .w80-mob
+ .w90-mob
+ .w100-mob

#### Order<a name="order"></a>

##### Tablet
+ .tab-order-1
+ .tab-order-2
+ .tab-order-3
+ .tab-order-4
+ .tab-order-5
+ .tab-order-6
+ .tab-order-7
+ .tab-order-8
+ .tab-order-9


##### Mobile
+ .mob-order-1
+ .mob-order-2
+ .mob-order-3
+ .mob-order-4
+ .mob-order-5
+ .mob-order-6
+ .mob-order-7
+ .mob-order-8
+ .mob-order-9

#### Alignment<a name="alignment"></a>
##### To Align All Modules Within a Container (Apply to container)<a name="container-alignment"></a>
+ .align-left 
+ .align-center 
+ .align-right 
+ .align-top
+ .align-middle 
+ .align-bottom 
+ .align-stretch 


##### To Align Individual Modules (Apply to module)<a name="module-alignment"></a>
+ .self-align-top
+ .self-align-middle 
+ .self-align-bottom
+ .self-align-left
+ .self-align-right

#### Padding<a name="padding"></a>
##### All Four Sides
+ .pxs, .padding-mini (8px)
+ .ps, .padding-small (15px)
+ .pm, .padding-medium (30px)
+ .pl, .padding-large (50px)

##### Top
+ .ptxs, .padding-top-mini (8px)
+ .pts, .padding-top-small (15px)
+ .ptm, .padding-top-medium (30px)
+ .ptl, .padding-top-large (50px)

##### Right
+ .prxs, .padding-right-mini (8px)
+ .prs, .padding-right-small (15px)
+ .prm, .padding-right-medium (30px)
+ .prl, .padding-right-large (50px)

##### Bottom
+ .pbxs, .padding-bottom-mini (8px)
+ .pbs, .padding-bottom-small (15px)
+ .pbm, .padding-bottom-medium (30px)
+ .pbl, .padding-bottom-large (50px)

##### Left
+ .plxs, .padding-left-mini (8px)
+ .pls, .padding-left-small (15px)
+ .plm, .padding-left-medium (30px)
+ .pll, .padding-left-large (50px)

#### Margin<a name="margin"></a>
##### All Four Sides
+ .mxs, .margin-mini (8px)
+ .ps, .margin-small (15px)
+ .pm, .margin-medium (30px)
+ .ml, .margin-large (50px)

##### Top
+ .mtxs, .margin-top-mini (8px)
+ .mts, .margin-top-small (15px)
+ .mtm, .margin-top-medium (30px)
+ .mtl, .margin-top-large (50px)

##### Right
+ .mrxs, .margin-right-mini (8px)
+ .mrs, .margin-right-small (15px)
+ .mrm, .margin-right-medium (30px)
+ .mrl, .margin-right-large (50px)

##### Bottom
+ .mbxs, .margin-bottom-mini (8px)
+ .mbs, .margin-bottom-small (15px)
+ .mbm, .margin-bottom-medium (30px)
+ .mbl, .margin-bottom-large (50px)

##### Left
+ .mlxs, .margin-left-mini (8px)
+ .mls, .margin-left-small (15px)
+ .mlm, .margin-left-medium (30px)
+ .mll, .margin-left-large (50px)

## Usage Examples

#### One column, half-page wide, centered
```html
<section class = "banner" id = "banner-three-columns">
	<div class = "container align-center">
		<div class = "module w50">
			<!-- content -->
		</div>
	</div>
</section>
```


#### Three column grid

```html
<section class = "banner" id = "banner-three-columns">
	<div class = "container align-center">
		<div class = "module w33">
			<!-- module equal to 33% of container -->
		</div>

		<div class = "module w33">
			<!-- module equal to 33% of container -->
		</div>

		<div class = "module w33">
			<!-- module equal to 33% of container -->
		</div>
	</div>
</section>
```

#### Sub-columns/Nested Columns

```html
<section class = "banner" id = "banner-sub-column">
	<div class = "container align-center">
		<div class = "module w50">
			<!-- module equal to 50% of container -->
		</div>

		<div class = "module w50">
			<div class = "container">
				<!-- Note that any modules inside modules must be wrapped in a container -->

				<div class = "module w40">
					<!-- sub column equal to 40% of its parent module -->
				</div>
				<div class = "module w60">
					<!-- sub column equal to 60% of its parent module -->
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
		<div class = "module w80">
			<!-- content -->
		</div>

		<div class = "module w20 padding-left">
			<!-- 	
				This wrapper module with a padding-left class creates some
				space between the adjacent module and the actual content 
				of this module
			-->
			<div class = "container">
				<div class = "module w100 panel padding-medium">
					<!--
						The panel class creates a background color to differentiate
						it from any other content, and the padding-medium will create
						space around the text content inside this module.
					-->
				</div>
			</div>
		</div>
	</div>
</section>
```

#### Full width / edge extended panel

Notice the slightly different container element. The panel class can be applied to both module elements for a split screen color effect.

```html
<section class = "banner" id = "banner-special-case">
	<div class = "container-extender align-center">
		<!-- 
			The container-extender class creates a container that spans the full width
			of the parent banner. There is no max-width. This means it's content will
			also extend this wide.
		-->
		<div class = "module w50 panel pm">
			<!-- content -->
		</div>

		<div class = "module w50 pm">
			<!-- content -->
		</div>
	</div>
</section>
```

If this is not the desired behavior, for example: you may want the background style on each half of the page to extend to the edge of the page, but you want the content in each half to be bound by a normal container, then you can use this approach:

```html
<section class = "banner" id = "banner-special-case">
	<div class = "container-extender align-center">
		<div class = "module w50 panel">
			<!-- altering the width of this module will shift the bound 1300px container left or right -->
			<div class = "container align-right">
				<div class = "container-inner">
					<!-- the container-inner element is automatically bound based on the size of its parent -->
					<div class = "module w100 pm">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
					</div>
				</div>
			</div>	
		</div>

		<div class = "module w50">
			<div class = "container align-left">
				<div class = "container-inner">
					<div class = "module w100 pm">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
					</div>
				</div>
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
