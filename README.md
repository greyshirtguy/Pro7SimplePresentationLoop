# Pro7SimplePresentationLoop
A crude and simple "digital signage" experiment for Pro7 all contained in a single .html file.

This simple web page will connect to Pro7 (via new API in 7.9+) and for the specified presentation/library, it will get images of the all slides and then roll through a looping display of those slide images.

This is super simple and crude - but lightweight enough to run on little PC sticks/Raspberry Pi's
You will want to setup the web-browser to run this .html file in fullscreen mode (and at computer startup).

1. Copy simpleloop.html to a computer (on same network as Pro7).
2. Update the follow values in the script code to suit your setup:
```
/*********** UPDATE THESE TO SUIT YOUR PRO7 SETUP *********************/
var ipAddressOfProPresenterComputer = "192.168.1.7"; // Hostname can used used here also if you have hostname resolution for your ProPresenter computer
var networkPortOfProPresenter = "50001"; // See ProPresenter network prefences
var libraryName = "Signage"; // Name of library with presentations to be used as simple digital signage
var presentationName = "Lobby Loop"; // Name of presenation (within library above) to run as simple slide show
var slideQuality = "1920"; // Width of image in pixels
var slideTime = 3; // Number of seconds to show each slide.
var transitionTime = 0.5; // Number of seconds to dissolve between each slide
var refeshPollTime = 10;  // Number of seconds to wait before polling the presentation to check if it has any changes! (be careful not to impact the performance of your pro7 machine by polling the presentation too often!)
/**********************************************************************/
```
3. Setup the computer to open this file in a web-browser, full-screen at startup.

As far as I can tell, it will download the images once and cache them until the webpage is reloaded (or the presentation changes)

TODO: Add auto retry for when Pro7 is not running and page tried to refresh/load
