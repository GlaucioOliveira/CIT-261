## Code Topic Fluency 

### HTML5 Tags
> Video, Audio, and Canvas Tags.

HTML5 introduced new tags that deals with multimedia (Video, Audio and Canvas). With the usage of these tags (`<video>`, `<audio>`, `<canvas>`) we can create HTML pages with rich features without needing any external component (like Flash).

#### Video

To add a Video to a HTML page, we need to add the `<video>` tag and specify the source of the video on the `src` attribute. The supported video types depends on the browser. ([Types of videos supported by browsers](https://developer.mozilla.org/en-US/docs/Web/HTML/Supported_media_formats)). The most common are .mp4 and .webm formats.

Below there is an example of a video with two possible sources (.mp4 or .webm) and also two buttons, one to pause and the other to play the music. Since there is the 'autoplay' attribute on the `<video>` tag, the video will start automatically as the page loads.

````html
<script>
 var videoPlayer = document.getElementById('player');

 function pauseVideo(){
   videoPlayer.pause();
 }

 function playVideo(){
   videoPlayer.play();
 }
</script>

 <video autoplay width="320" height="180" controls id="player">
  <source src="http://goliveira.com/byui/resources/jack-johnson-in-the-morning.mp4" type="video/mp4">
  <source src="http://goliveira.com/byui/resources/jack-johnson-in-the-morning.webm" type="video/webm">
  Oops, no suport for .mp4 or .webm videos. Try another browser :(
</video> 

<div>
<button onclick="playVideo()">Play</button>
<button onclick="pauseVideo()">Pause</button>
</div>
````

<a href="https://codepen.io/glaucioso/pen/oVodGP" target="_blank">Live Demo (at CodePen)</a>

We can access properties (like current position, buffered data) and fire events with the video tag (like play or pause a video). 
[Here you can find all the properties and events avaliable](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video#Attributes).


#### Audio

To add an Audio to a HTML page what we need is to add the `<audio>` tag. It's funcionality is similar to the video tag. We can access properties and events associated with the Audio (current position, play, pause, seek position, etc) on the structure of the DOM Element of the Object (by grabbing them with the `document.getElementById` function). Below there is an example for this Tag:

````html
<script>
 var audioPlayer = document.getElementById('player');

 function pauseAudio(){
   audioPlayer.pause();
 }

 function playAudio(){
   audioPlayer.play();
 }
</script>

<audio controls id="player">
  <source src="http://goliveira.com/byui/resources/jack-johnson-in-the-morning.mp3" type="audio/mpeg">
  <source src="http://goliveira.com/byui/resources/jack-johnson-in-the-morning.m4a" type="audio/m4a">
  Oops, no suport for .mp3 or .m4a. Try another Browser :(
</audio>
<div>
<button onclick="playAudio()">Play</button>
<button onclick="pauseAudio()">Pause</button>
</div>
````
<a href="https://codepen.io/glaucioso/pen/bZzwVz" target="_blank">Live Demo (at CodePen)</a>


#### Canvas

With Canvas we are able to draw graphics on a HTML page using JavaScript. We can draw shapes, texts, lines, gradient effects in two dimensions (2D) or three dimensions (3D).

The first step to use this tag is to create the `<canvas>` tag, specify it's size (`width`, `height` attributes), and them use JavaScript to draw.

In the exemple below there is the drawning of two crossed lines:

````html
<canvas id="canvas" width="200" height="100">
</canvas>

<script>
 var canvas = document.getElementById("canvas");
 var drawingContext = canvas.getContext("2d");
 drawingContext.moveTo(0, 0);
 drawingContext.lineTo(200, 100);
 drawingContext.stroke(); 

 drawingContext.moveTo(200,0);
 drawingContext.lineTo(0, 100);
 drawingContext.stroke();
</script>
````
<a href="https://codepen.io/glaucioso/pen/OqdRmd" target="_blank">Live Demo (at CodePen)</a>

Once we get the drawning context (on the example the `drawingContext`), we are able to draw using the internal functions (functions like `moveTo`, `lineTo`, `stroke`, `'fillRect`). 

*NOTE:* [A list of all the avaliable functions and attributes can be found here](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D).

