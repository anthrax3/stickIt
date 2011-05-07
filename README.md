jQuery stickIt Plugin - v0.1.0
==============================
Dead-simple plug to enable "sticky elements". Attach an element to the
window's viewport such that it stays on the page when the user scrolls
down.  

_NOTE: This is pre-release software under active development! Not intended for use in production (yet)!_

_NOTE NOTE: Demo coming soon(ish)!_

Overview
--------
On page ready, stickIt wraps your target element with a invisible
place-holder container then monitors the scroll position to detect when
your element is being scrolled off the page. When your element is being
scrolled off page, stickIt simply adds a css class to your element so
that you can set a new display style of your choosing. The placeholder
element is also sized to match the now stuck target element so that the page doesn't bounce around.  

###highlights:###

+ Easy-peasy!
+ Works in IE7-9 and the _reasonable_ browsers too!
+ Customizable via regular ol' css and js!
+ Custom events to help integrate w/ yr own science!
+ Throttled scroll events!


Usage
-----

###basic###

    //initialize your element
    $("#myElement").stickIt();

- - -

###advanced###

    //configuration options
    $("#myElement").stickIt({
      containerClass : "stickItContainer", //class assigned to place-holder element
      enabledClass   : "stickItFixed", //class assigned to a stuck element
      resetEvent     : "reset.stickIt" //custom event to reset a stuck element
    });

- - -

###support files###
You'll need to remember to add rules to your css to style your stuck
element. Typically that looks something like this:

    .stickItFixed {
      position: fixed;
      top: 10px;
      left: 10px;
      width: 200px;
      height: 200px;
    }

- - -

License
-------
jQuery stickIt Plugin  
Copyright (c) 2011 Matthew Mirande  
Dual licensed under the MIT or GPL Version 2 licenses.
