---
layout: post
title:  "Background Image Fallbacks"
---

There is a new function called Image() that is currently not supported by any browswer,
but it allows for many cool features to be added to background images.
The Image() function allows us to:

1. Use media fragments to clip out a portion of an image

2. Use a solid color as an image

3. Fallback to a solid-color image, when the image at the specified url can’t be downloaded or decoded

4. Automatically respect the image orientation specified in the image’s metadata

The image() notation is defined as:

image() = image( <image-tags>? [ <image-src>? , <color>? ]! )
<image-tags> = [ ltr | rtl ]
<image-src> = [ <url> | <string> ]
