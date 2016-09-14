###Basic Structure

Each part of your page must be wrapped in a section element, with class 'banner'.
Inside each section, you will have a container. The container is set to a width of
90% with a max-width of 1200px but you can adjust this as you see fit.  

Inside each container, you create modules - your main content blocks/elements.  Modules within
a container will flow left to right. Apply an alignment class to your container
if the widths of its child elements do not add up to 100%.

```html
<section class = "banner">
	<div class = "container align-center">
		<div class = "module per100">
		</div>
	</div>
</section>
```

###'Painting' Styles

Familiarize yourself with the available classes.  Create more, or edit the existing
classes to your needs. Add the appropriate classes to your module block.

These classes govern module width, alignment, margin, padding, and font size,
weight, and decoration.  There are also stock classes for images and buttons.

Typical order of class application might be as follows:
width, panel, padding, margin, alignment, font styles

```html
<div class = "module per25 panel padding-small align-top">
	<!-- content here -->
</div>
```

###Usage Examples

####Three column grid

```html
<section class = "banner" id = "banner-three-columns">
	<div class = "container align-center">
		<div class = "module per33 align-top padding-small">
			<!-- content -->
		</div>
		<div class = "module per33 align-top padding-small">
			<!-- content -->
		</div>
		<div class = "module per33 align-top padding-small">
			<!-- content -->
		</div>
	</div>
</section>
```

####Sub-columns

```html
<section class = "banner" id = "banner-sub-column">
	<div class = "container align-center">
		<div class = "module per50 align-top padding-small">
			<!-- content -->
		</div>
		<div class = "module per50 align-top padding-small">
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