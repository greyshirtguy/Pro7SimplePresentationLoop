# Pro7SimplePresentationLoop
A crude and simple "digital signage" for Pro7 all contained in a single .html file.
Once setup, it will open a specific presentation, get images of the slides and then roll through a looping display of those slide images.
This is super simple and crude - but lightweight enough to run on little PC sticks/Raspberry Pi's
You will want to setup the web-browser to run this .html file in fullscreen mode (and at computer startup).

1. Copy simpleloop.html to a computer (on same network as Pro7).
2. Update the follow values in the script code to suit your setup:
```
var ipAddressOfProPresenterComputer = "192.168.1.7"; // Hostname can used used here also if you have hostname resolution for your ProPresenter computer
var networkPortOfProPresenter = "50001"; // See ProPresenter network prefences
var libraryName = "Signage"; // Name of library with presentations to be used as simple digital signage
var presentationName = "Lobby Loop"; // Name of presenation (within library above) to run as simple slide show
var slideQuality = "1920"; // Width of image in pixels
var slideTime = 3; // Number of seconds to show each slide.
var transitionTime = 0.5; // Number of seconds to dissolve between each slide
```
3. Setup the computer to open this file in a web-browser, full-screen at startup.
