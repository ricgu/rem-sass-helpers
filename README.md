# Rem sass functions

"Rem unit allows font size and other properties to be specified against the root element, not just the parent, as is the case for the em unit" 
(taken from http://www.sitepoint.com/css3-rem-units/).

With these functions, you can convert px units to rem. verty easly

## Usage

You can find `px-to-rem` function which just convert px to rem

	font-size: px-to-rem(16px);	

It returns `1rem`;

There is also a mixin called `make-property` that allows you to make both px and rem units for a property.
You have to pass a property name (example font-size, or margin) and as second parameter px or rem value.  
It will convert the unit for you:

	@include make-property(font-size, 16px);

The css output will be:

	font-size: 16px;
	font-size: 1rem;

Or you can pass rem:

	@include make-property(font-size, 1rem);

The css output will be:

	font-size: 16px;
	font-size: 1rem;

Is it possible to add multiple values as well:
	
	@include make-property(margin, 10px 15px);

You can also change the global variable `$base-font-size` as default it is set `16`.

