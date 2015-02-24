# Ost

Take pictures with the camera/webcam. Say cheese!

1. Take some pictures
2. Re-arrange the pictures inside the black border
3. Log in to Facebook
4. Share the photo collage on Facebook

Demo: http://donkarlssonsan.github.io/Ost

![Say cheese!](https://raw.githubusercontent.com/DonKarlssonSan/Ost/gh-pages/screenshots/ost_screenshot.png "Say cheese!")

### How it works

The video stream from the web cam is accessed with the getUserMedia JavaScript API. It is a new feature in HTML 5 and not implemented in all browsers yet. This is a good overview of current browser support: http://caniuse.com/#feat=stream

When taking still photos from the video stream, a hidden canvas is used to get a base64 encoded string representation of the photo which is then added to the DOM as a normal img element.

The [html2canvas](https://github.com/niklasvh/html2canvas) library is used to generate an image of the collage when posting to Facebook.

For Facebook integration there are two parts: 
1. The Facebook JavaScript SDK is used for logging in. 
2. The low level HTTP-based Graph API is used for posting images.

### TODO
 * Make it look nice!
 * Add options for applying CSS filters on the video stream.
 * Have a fallback for browsers lacking native support: https://github.com/addyosmani/getUserMedia.js/
