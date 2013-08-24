#DEMO

Checkout a demo here:
[http://hadimichael.github.io/gest.js/demo.html](http://hadimichael.github.io/gest.js/demo.html);

#USAGE

You will need to include the 'gest.js' script in your index &lt;head&gt;, using something like:

<pre><code>&lt;script type="text/javascript" src="gest.js"&gt;&lt;/script&gt;</pre>

Starting gest.js and handling gestures:
<pre><code>document.addEventListener('gest', function(gesture) {
	if (gesture.ready) {
		gest.start(); //start gesture detection
	} else {
		//handle gesture .direction .up .down .left .right here...
		document.getElementById('mydiv').innerHTML = gesture.direction;
	}
}, false);
gest.start();
</code></pre>

To stop gesture detection, use:
<pre><code>gest.stop();</code></pre>

Toggle debug mode using:
<pre><code>gest.debug([boolean]);</code></pre>

Other available options:
Enable/disable skin filtering
<pre><code>gest.options.skinFilter = [boolean]; //default is false</code></pre>

Enable/disable on screen messages
<pre><code>gest.options.messages = [boolean]; //default is true</code></pre>

#TODO

- Write up proper documentation
- Better Firefox support...

#LICENSE (MIT)

Copyright (c) 2013, Hadi Michael (http://hadi.io)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

##Attribution
This library was inspired by work from Willy Wu [https://github.com/willy-vvu](https://github.com/willy-vvu).