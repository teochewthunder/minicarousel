# The Mini-carousel

This little HTML/CSS/JavaScript trick achieves the illusion of seamlessness for a scrolling marquee gallery.

## HTML/CSS
A div containing several other container divs, all lined up and floated left. It takes up 100% of screen width, and the `overflow` property is set to `hidden`.

It contains a div (styled using `carouselitems`) that is 200% of screen width. However, since its parent's `overflow` property is set to `hidden`, only 100% will be shown at any one time. It contains five divs, styled using `carouselitem`.

Each div styled using `carouselitem` takes up 20% of screen width, which is actually 10% of the parent's (which takes up 200% of screen width) width. Within these divs are pictures and contents.

## JavaScript
The `duplicate()` copies all the divs styled using `carouselitem` and inserts them into the same parent. This is why each is 10% of the parent's width. Because then you will now have 10 divs, each at 10%, making up 100%.

## CSS animation
The CSS animation moves the div styled using `carouselitems` left 100%, and then stops. And repeats. However, the transition is so quick that it appears that the marquee is never-ending.

Also, on mouseover, the animation pauses. From here, it is possible to attach more actions to the mouse click.
