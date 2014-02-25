sPreloader
===========

Preload images, even in CSS background. This is custom version of QueryLoader2 by Gaya Design.

Read the full post here: http://www.gayadesign.com/diy/queryloader2-preload-your-images-with-ease/

How to use
----------

Include the script in the head section of your webpage.

	<script src="path/to/file/jquery.queryloader2.js" type="text/javascript"></script>

Be sure to add it after you include jQuery.

Now call QueryLoader in a $(document).ready() like this:

	$(document).ready(function () {
		$("body").queryLoader2();
	});
	
For support on iOS devices use the following code:

	window.addEventListener('DOMContentLoaded', function() {
		$("body").queryLoader2();
	});

Install using Bower
-------------------

	bower install queryloader2

Basic usage
-----------

    $(selector).queryLoader2(options);
	
Options
-------

**backgroundColor**

(string) background color of the loader (in hex).
Default: "#000"
	
**barColor**

(string) background color of the bar (in hex).
Default: "#FFF"

**barHeight**

(int) Height of the bar in pixels.
Default: 1

**completeAnimation**

(string) set the animation type at the end. Options: "grow" or "fade".
Default: "fade"

**minimumTime**

(int) time in miliseconds which the loading has to run. If time has not passed the animation will still show.
Default: 500

**deepSearch**

(boolean) set to true to find ALL images with the selected elements. If you don't want queryLoader to look in the children, set to false.
Default: true
	
**percentage**

(boolean) Set to true to enable percentage visualising.
Default: false

**onComplete**

(function) this function is called once the loading and animation are completed.
Default: none

**onLoadComplete**

(function) this function is called once the loading is completed, before the ending animation.
Default: none


Salipro Custom
-------------
I added some options to enhance customize.


**hideOverlay**

> type: boolean, default: false

Set `true` if you want to hide default-overlay of QueryLoad2

**customOverlay**

> type: object, default: {}

You had a overlay element, if you want QueryLoad2 to use it, plz leave id:

```
customOverlay: {
     overlayId: 'preloader'
}
```

Override CSS of element with object like jQuery
```
customOverlay: {
     overlayStyle: { top: '10%', left: '50%',... },
     barStyle: {...},
     percentageStyle: {...}
}
```


Thanks to
---------
QueryLoader2 by Gaya
