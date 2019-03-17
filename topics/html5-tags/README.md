## Code Topic Fluency 

### HTML5 Tags
> Video, Audio, and Canvas. (INCOMPLETE...)

HTML5 introduced new tags that deals with multimedia (Video, Audio and Canvas). With them, we can expose into a web page rich content without the need of any component (like Flash or Java Applet).

#### Video
````html
 <video autoplay width="320" height="180" controls>
  <source src="https://download.blender.org/peach/bigbuckbunny_movies/BigBuckBunny_320x180.mp4" type="video/mp4">
  <source src="https://download.blender.org/peach/bigbuckbunny_movies/big_buck_bunny_480p_stereo.ogg" type="video/ogg">
  Oops, no suport for mp4 or ogg :|
</video> 
````
<a href="https://codepen.io/glaucioso/pen/oVodGP" target="_blank">Live Demo (at CodePen)</a>


#### Audio
````html
<audio controls>
  <source src="https://www.w3schools.com/tags/horse.ogg" type="audio/ogg">
  <source src="https://www.w3schools.com/tags/horse.mp3" type="audio/mpeg">
  Oops, no suport for ogg or mp3 :|
</audio>
````
<a href="https://codepen.io/glaucioso/pen/oVodGP" target="_blank">Live Demo (at CodePen)</a>


#### Canvas
````html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;">
</canvas>
````
<a href="https://codepen.io/glaucioso/pen/oVodGP" target="_blank">Live Demo (at CodePen)</a>
