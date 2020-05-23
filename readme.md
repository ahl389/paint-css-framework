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

Paint handles all of the file imports into `paint.scss` for you.

`paint.scss` is the primary file with the majority of Paint's relevant code. 

`reset.scss` contains all the basic CSS resets so can Paint can start with its own clean slate. 

`variables.scss` defines the basic set of variables used throughout Paint. It's common that you might want to modify these values to best suit your needs, or add new variables in this file to support your custom CSS.

`custom.scss` is an additional empty file preloaded into `paint.scss` and is the appropriate location for all custom CSS you want to layer on top of Paint. 

### CSS

Don't want to use SCSS? No problem: head to `src/CSS` and download the `paint.css` file - this contains everything that's in the `.scss` version, but does not offer the flexibility of variables and easier modifications.


## Getting Started with Paint
Paint is fast because with it, you can layout and build a page almost entirely with HTML. 
Your styles are 'painted' on to your HTML elements via a series of basic CSS classes.  
For this to work, your HTML must be structured using Paint's basic building blocks: [`banner`](#banner), [`container`](#container), and [`module`](#module).

We'll go through each of  these below: 

### Banner

Banners are page-wide elements that you use to organize and divide the major content of your webpage vertically. 
As a general rule, if you want to use a different background, or use a new subtitle on a page, you probably want to create a new `banner`.

To create a `banner`, make a `section` HTML element, and give it the class `banner`.  

```html
<section class = "banner" id = "banner-your-id">
</section>
```

> Note: Banner elements don't get `painted`! But it's likely that you'll want to give them an `id` or special `class` to add background styling or custom padding sizes.

#### Container

Within each section block, you will have immediately have a `div` element with the class `container`.  

The default container element is set to 90% of the page width, is centered, and has a max-width of 1200px. 
If you'd prefer different universal `container` settings, feel free to change them in `variables.scss`.

```html
<section class = "banner" id = "banner-your-id">
	<div class = "container">
	</div>
</section>
```

Container elements can be painted with the following types of classes (see [classes](#classes) section):
+ [Fonts & Text](#fonts-and-text)
+ [Content Alignment within Containers](#container-alignment)

> Note: Fonts & Text classes should only be applied to `container` elements if you want these classes to affect every child element within the container. 
>If not, save these for `module` elements.

#### Module

`Module` elements are created inside container elements.
`Modules` are your basic content block/element.
`Modules` will automatically flow from left to right. 
In most use cases, you will paint them with a `width` class, but it's not required. 
If you don't paint them with a `width` class, then they assume their natural width. This is useful when creating navigation bars, for example.

```html
<section class = "banner" id = "banner-your-id">
	<div class = "container">
		<div class = "module w50">
		</div>
	</div>
</section>
```

You can assign any or all of the following [class types](#classes) to `module` elemens:
+ [Fonts & Text](#fonts-and-text) (Note: These will be applied to the entire contents of the module)
+ [Individual Module Alignment within Container](#module-alignment)
+ [Module Width](#width) (Including Module Width on Tablet and Mobile)
+ [Module Order](#order) (Including Module Order on Tablet and Mobile)
+ [Padding](#padding)
+ [Margin](#margin)

Like `banner` elements, adding an `id` to your `module` elements is recommended.

## Classes

Paint's classes govern module width, alignment, margin, padding, along with font size, weight, and decoration.  
Paint comes with basic classes for `img` and `button` elements, and very basic styles for `h`, `p`, and `a` elements.

In order to keep your code consistent, Paint recommends applying classes in this order:

`width`, `panel`, `alignment`, `padding`, `margin`, `font & text` 

```html
<div class = "module w80 panel ps mr mb">
	<h3 class = "bold">H3 Heading</h3>
	<p class = "mr italic">Content</p>
</div>
```

### Building Blocks

| Class Name |
| ------------ |
| `banner` | 
| `container` | 
| `container-extender` | 
| `module` |

### General

| Class Name |
| ------------ |
| `button` | 
| `panel` | 
| `panel highlight` | 


### Fonts and Text

#### Font Size
| Class Name | CSS Property:Value | Default |
| ------------ | ------------ | ------------ |
| `mini` | font-size: .6em | no |
| `small` | font-size: .8em | no |
| `medium` | font-size: 1em | yes |
| `large` | font-size: 1.25em | yes |
| `xl` | font-size: 1.75em | no |
| `x2` | font-size: 2.5em | no |
| `x3` | font-size: 3.5em | no |
| `x4` | font-size: 4em | no |

#### Capitalization and Text Effect
| Class Name | CSS Property:Value | Default |
| ------------ | ------------ | ------------ |
| `uppercase` | text-transform: uppercase | no |
| `lowercase` | text-transform: lowercase | no |
| `capitalize` |  text-transform: capitalize | no |
| `bold` | font-weight: bold | no |
| `italic` | font-style: italic | no |

#### Text Alignment
| Class Name | CSS Property:Value | Default |
| ------------ | ------------ | ------------ |
| `text-left` | text-align: left | yes |
| `text-right` | text-align: right | no |
| `text-center` | text-align: center | no |



### Module Width<a name="width"></a>
Each of these classes indicate a percentage width (the `w` in front of each number is for `width`) relative to the `module's` parent container.  
Adding a padding class to any module will *not* alter its outer width - pad away, no math necessary!

Paint applies width from a desktop-first perspective, with default behaviors for seamless responsive changes on tablet and mobile:
All width classes will cascade on tablet but default to full-width on mobile, unless otherwise specified.

If you want a module to have a different width on mobile or tablet, you have to add the corresponding tablet/mobile width class.
You may apply a desktop, tablet, and mobile width class to any element.

##### Desktop

| Class Name | CSS Property:Value | Default | Tablet Width | Mobile Width | 
| ------------ | ------------ | ------------ | ------------ | ------------ |
| `.w10` | width: 10% | no | `.w10-tab` | `.w10-mob` |
| `.w15` | width: 15% | no | `.w15-tab` | `.w15-mob` |
| `.w20` | width: 20% | no | `.w20-tab` | `.w20-mob` |
| `.w25` | width: 25% | no | `.w25-tab` | `.w25-mob` |
| `.w30` | width: 30% | no | `.w30-tab` | `.w30-mob` |
| `.w33` | width: 33.333% | no | `.w33-tab` | `.w33-mob` |
| `.w35` | width: 35% | no | `.w35-tab` | `.w35-mob` |
| `.w40` | width: 40% | no | `.w40-tab` | `.w40-mob` |
| `.w45` | width: 45% | no | `.w45-tab` | `.w45-mob` |
| `.w50` | width: 50% | no | `.w50-tab` | `.w50-mob` |
| `.w55` | width: 55% | no | `.w55-tab` | `.w55-mob` |
| `.w60` | width: 60% | no | `.w60-tab` | `.w60-mob` |
| `.w65` | width: 65% | no | `.w65-tab` | `.w65-mob` |
| `.w66` | width: 66.667% | no | `.w66-tab` | `.w66-mob` |
| `.w70` | width: 70% | no | `.w70-tab` | `.w70-mob` |
| `.w75` | width: 75% | no | `.w75-tab` | `.w75-mob` |
| `.w80` | width: 80% | no | `.w80-tab` | `.w80-mob` |
| `.w85` | width: 85% | no | `.w85-tab` | `.w85-mob` |
| `.w90` | width: 90% | no | `.w90-tab` | `.w90-mob` |
| `.w95` | width: 95% | no | `.w95-tab` | `.w95-mob` |
| `.w100` | width: 100% | no | `.w100-tab` | `.w100-mob` |

##### Example
```html
<section class = "banner" id = "banner-your-id">
	<div class = "container">
		<div class = "module w50 w70-tab">
			<!-- 
				this module will be:
				- 50% of its parent width on deskop
				- 70% of its parent width on tablet
				- 100% of its parent width on mobile
			-->
		</div>
	</div>
</section>
```



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
