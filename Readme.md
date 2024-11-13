-make an app with the canvas stretch the whole screen allowing user to drawing anywhere, but only rendering content at the middle inside the box.

//innerWidth js property return the interior width of the window in px (the width of the window's layout viewport)
//innerHeight js property return the interior height of the window in px

-add event listener to the whole app
-the canvas is positioned above everything in the app.
-add point to our shapes anytime we click the mouse on the screen to draw.
-finally add bezier curves to the app.
-only collect point after clicking on the screen, not just basically moving or hovering the mouse over the screen => move others event into the callback function that handle the pointdown event.

-only want to render shapes after the pointUp event fired, not just collecting all path and then keeping rendering them all after each event => create a shape array to collect all path after each pointUp event fired, and then give the "path" variable back to an empty array to collect new paths for next shapes to render new shapes after next pointUp events fired.

-only want to render shapes but not let them stack onto each other after each rendering => just clear the previous rect and then recreate a new one before rendering a new shape.

//draw a rectangle
