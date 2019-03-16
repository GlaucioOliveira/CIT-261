## Code Topic Fluency 

### CSS3 Animations
> Designing, Defining, and Triggering CSS3 Animations without Custom Libraries.

With CSS Animations we are able to create animations with HTML elements without the need of a custom library. The difference between CSS Animations and [CSS Transition](../css3-transitions/README.md) is that on the Animations we are able to specify what will happen at a specific time of the animation (using `@keyframes`), This is not possible with Transition alone.

````css
/* Example of a keyframe */
@keyframes breaking-news-animation {
  0%   {background-color: black;}
  50%  {background-color: #721c24;top:-10px;}
  100% {background-color: black;}
}
````

In the example above there is the animation named `breaking-news-animation`. For a HTML Element have this animation, it's necessary to specify the property **animation-name** on the CSS Selector of the element, and also we need to specify the time that this animation will take with the **animation-duration** property. We can also delay the animation with the usage of the **animation-delay** property.

Below there is an example showing the above animation in action:

````html
<style>
  @keyframes floating-left-animation {
  0%   {padding-left:10%;}
 }
  
@keyframes breaking-news-animation {
  0%   {background-color: black;}
  50%  {background-color: #721c24;top:-10px;}
  100% {background-color: black;}
}

.notice {
  animation-name: floating-left-animation, breaking-news-animation;
  animation-duration: 2s, 3s;
  animation-delay: 1, 3;
  animation-iteration-count: 1, infinite;
  color:white;
  overflow:hidden;
  height:40px; 
  padding: 15px;
  font-family: Helvetica;
</style>
<body>
  <h1 class="notice">Breaking News</h1>
  <div id="content">
    <h2>CSS3 is amazing. We can create nice effects with it.</h2>
  </div>
</body>
}
````
<a href="https://codepen.io/glaucioso/pen/XGqeeR" target="_blank">Live Demo (At CodePen)</a>

**NOTE**: To allow the animation to be executed more then one time we can use the **animation-iteration-count** property. To allow the effect occurr without end just pass the `infinite` value to this property.
