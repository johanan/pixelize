#Pixelize

This library came about from an the idea of what a browser would look like on the NES. Of course every image it showed would be pixelized. 

It uses two canvas elements to accomplish this. The first canvas scales the image down and the next canvas scales it back up. A little math is used to determine the scale ratio, but other than that it is pretty straight forward.

I have used a few ideas from https://github.com/desandro/close-pixelate (I use essentially the same function to test for canvas support and the idea to add the function off the img element itself). Close Pixel has more artistic options, but this library is a simple scale down and then back up.

##Examples

The first few photos of pixelate.html show you what the library does. The next two pictures show you that you can specifiy your own scale ratio.

##Example Code

All you need to do is call pixelize on an image element. There is only one option - scale ratio. It takes a percentage as a decimal. If you do not specify a scale ration it will automatically calculate based on the images dimensions.

```javascript
//auto calculating
var getImage = document.getElementById('image').pixelize();

//set the scale ratio
var setScaleRatio = document.getElementById('image').pixelize(.25);

//that's it!
```