# [jCider](http://pratinav.tk/jCider)
An extensive and responsive jQuery carousel plugin that will slide your world.

##Contribution and Issues
This plugin is early in development and new features will be added soon. Feel free to contribute by sending in [pull requests](http://github.com/Pratinav/jCider/pulls) and help me improve the plugin by pointing out bugs in the [issues page](http://github.com/Pratinav/jCider/issues). 
####Pull Requests
Feel free to send in [pull requests](http://github.com/Pratinav/jCider/pulls) to improve the plugin or add new features. If you want to add a new feature please send in a clear and elaborate description and explanation of the working of it and a [codepen](http://codepen.io) or [jsFiddle](http://jsFiddle.net) demostrating your feature. Your feature has to be compatible with all other features and settings available. 
####Issues
The [issues page](http://github.com/Pratinav/jCider/issues) is **ONLY** for bugs or problems with the plugin or discussions for adding new features.   
If you have a problem to operate the plugin or set it up, the issues page is not the place for it, mail me at [pratinavbagla@gmail.com](mailto:pratinavbagla@gmail.com). **I will try to get to you as fast as possible but may not be able to get to you always.**


##Installation   

####CDN
- Link the ```jcider.css``` file in your ```head``` tag, like this: 
```
<link rel="stylesheet" href="//cdn.jsdelivr.net/jquery.jcider/3.0.1/jcider.css"/>
```
- Link ```jcider.min.js``` in your ```head``` tag or at the end of your ```body``` tag.
 **Don't forget to link [jQuery](https://jquery.com) before the jCider file.**   
**If you want touch and swipe support link the ```jquery.mobile.custom.min.js``` file as well.**

Like this:

```
<script type="text/javascript" src="//code.jquery.com/jquery-1.11.3.min.js"></script>
// Only if you want swipe support
<script type="text/javascript" src="PATH_TO_FILE/jquery.mobile.custom.min.js"></script>
<script type="text/javascript" src="//cdn.jsdelivr.net/jquery.jcider/3.0.1/jcider.min.js"></script>
```


####Download files   
- Download the files.
- Link the ```jcider.css``` file in your ```head``` tag, like this: 
```
<link rel="stylesheet" href="PATH_TO_FILE/jcider.css"/>
```
- Link ```jcider.min.js``` or ```jcider.js``` in your ```head``` tag or at the end of your ```body``` tag.
 **Don't forget to link [jQuery](https://jquery.com) before the jCider file.**   
**If you want touch and swipe support link the ```jquery.mobile.custom.min.js``` file as well.**

Like this:

```
<script type="text/javascript" src="//code.jquery.com/jquery-1.11.3.min.js"></script>
// Only if you want swipe support
<script type="text/javascript" src="PATH_TO_FILE/jquery.mobile.custom.min.js"></script>
<script type="text/javascript" src="PATH_TO_FILE/jclider.min.js"></script>
```


####Package Managers
For [Bower](http://bower.io)-   
```bower install --save jcider``` 

For [NPM](http://npmjs.com)-   
```npm install jcider```   


####Styles
The styles in the ```jcider.css``` file are the default styles that come with the plugin. You can customize the appearence and positioning as per your convinience in the ```jcider.css``` file. Please refer to the file for information on the selectors.



##Usage
####HTML
The carousel uses a 3 layer structure in the HTML document. For, example-
```
<div class="slider">
	<ul>
		<li>First Slide</li>
		<li>Second Slide</li>
		<li>Third Slide</li>
	</ul>
</div>
```

This is not limited to any specific elements or Class/ID names. So this too can be used-
```
<div class="another-slider">
	<div>
		<div>First Slide</div>
		<div>Second Slide</div>
		<div>Third Slide</div>
	</div>
</div>
```
All your content for each slide should go inside the innermost elements, as illustrated above.

_For the rest of the docs we will refer to the outermost element as the **wrapper**, the middle element as the **slider** and the innermost elements as the **slides**._


####CSS
Do not give the **'slides' (innermost elements)** any width or height. The width and height given to the **'wrapper' (outermost element)**, will be given to the slides automatically.

You can style each slide through the selector for the **slide elements**.


####Basic Usage
Put the following code in ```script``` tags in the ```head``` tag of your HTML document.
```
$(document).ready(function(){
	// Make sure to call jcider on the wrapper element
	$('yourWrapperElementHere').jcider();
});
```
> Make sure to call ```.jcider()``` on the wrapper element. 


####Advance Usage- Settings
You can pass in multiple options as arguments for the ```.jcider()``` function. They are- 
```
$('yourWrapperElementHere').jcider({
	visibleSlides: 1,
	fading: false,
	easing: 'ease-in-out',
	controls: true,
	pagination: true,
	transitionDuration: 400,
	autoplay: false,
	slideDuration: 3000
});
```
| Setting Name | Value | Description | Default |
|--------------|-------|-------------|---------|
| visibleSlides | integer | Selects the number of slides visble at a time. | 1 |
| fading | boolean | Selects the type of transition. true is fading. ```false``` is sliding. | false |
| easing | string | Selects the type of easing to be used for CSS animations. | 'ease-in-out' |
| controls | boolean | Chooses whether the navigation controls are visible or not. ```true``` is visible. | true |
| pagination | boolean | Chooses whether the pagination is visible or not. ```true``` is visible. | true |
| transitionDuration | integer | The duration taken to transition from one slide to another, in milliseconds. | 400 |
| autoplay | boolean | Chooses whether automatic transition between slides is on or off. ```true``` is on. | false |
| slideDuration | integer | The duration between change of slides, in milliseconds. Only applicable if autoplay is on. | 3000 |


####Using Multiple carousels in one page
You can use multiple carousels in one page with ease. There may be two or more sliders with the same class.

For example your **HTML** would be-
```
<div class="slider">
	<ul>
		<li>First Slide.</li>
		<li>Second Slide.</li>
		<li>Third Slide.</li>
	</ul>
</div>

<div class="slider">
	<ul>
		<li>First slide.</li>
		<li>Second slide.</li>
		<li>Third slide.</li>
	</ul>
</div>

<div class="another-slider">
	<ul>
		<li>First Slide.</li>
		<li>Second Slide.</li>
		<li>Third Slide.</li>
	</ul>
</div>

<div class="another-slider">
	<ul>
		<li>First Slide.</li>
		<li>Second Slide.</li>
		<li>Third Slide.</li>
	</ul>
</div>
```

Your **JavaScript** would be-
```
$('.slider').jcider();
$('.another-slider').jcider();
```

##Dependencies
[jQuery](https://jquery.com) - **Using the lastest version is recommended**

**Optional** Custom jQuery-mobile (included)



##License
Copyright (c) 2015 Pratinav Bagla

This content is released under [The MIT License](http://github.com/Pratinav/jCider/blob/master/LICENSE.txt).


_See a typo? Think docs can be improved? Send in a [pull request](http://github.com/Pratinav/jCider/pulls) or tell me in the [issues page](http://github.com/Pratinav/jCider/issues)._
