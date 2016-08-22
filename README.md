# jquery.stepper.js
> Lightweight input stepper. [Check it out on JSFiddle](http://codepen.io/anon/pen/ZONpxW?editors=0010)

## Features
- Works on input type="text"
- Set initial values in the markup or Javascript
- Optionally configure min/max values with attributes

## Install
Download and include the javascript file.
```html
<script src="jquery.stepper.js"></script>
<link href="style.css" media="all" rel="stylesheet" />
```

## Basic usage
Check out `index.html` for all examples.

```html
<div class="stepper" id="stepper_1">
  <div class="stepper-progress"></div>
  <input type="text" class="stepper-number">
</div> 
```

Call the input stepper plugin on the desired selector

```javascript
$(function () {
	// Document ready
	$('#stepper_1').stepper();
});
```

## Advanced usage

```html
<div class="stepper" id="stepper_2">
  <div class="stepper-progress"></div>
  <input type="text" class="stepper-number" min="10" max="90">
</div>
```

Override properties like the input stepper plugin on the desired selector

```javascript
$('#stepper_3').stepper({
	selectorProgressBar: '.stepper-progress',
	selectorInputNumber: '.stepper-number',
	classNameChanging: 'is-changing',
	decimals: 2,
	unit: 'px',
	initialValue: 50,
	min: -200,
	max: 200,
	stepSize: 5
});

```

## Default settings
The input stepper can be called with a number of options. The defaults of each option are listed below

```javascript
$('.input-stepper').inputStepper({

	// Values in the markup always overwrite this settings
	// min and max value can be overridden with the attribute on the input text
	// if there is no initial value defined, the plugin take the max value
	initialValue: null,
	min: 0,
	max: 100

	// The selector for the input
	selectorInputNumber: '.stepper-number',

	// The selector for the progress bar
	selectorProgressBar: '.stepper-progress',

	// The class used when you have the focus+moving the cursor on the input text field
	classNameChanging: 'is-changing',

	// Number of decimals to display
	decimals: 0,

	// unit to concatenate with the value result
	unit: '%',

	// Step used to increaste the progress bar.
	// Increase this value if you have a big range. Reduce the value (ex : .25) if you have a small range
	stepSize: 1
});
```
