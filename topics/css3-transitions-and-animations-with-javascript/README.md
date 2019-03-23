## Code Topic Fluency 

### CSS3 Transitions and Animations with JavaScript
> Creating CSS3 Transitions and Animations in CSS and triggering them with JavaScript.

With JavaScript we are able to trigger [Animations](../css3-animations/README.md), [Transformations](../css3-transforms/README.md) and [Transitions](../css3-transitions/README.md).

This possibility allows effects to happen according to what we define at JavaScript code or through user interaction. In the Example below, there is an effect that writes a 'loading' on the screen. But this animation will only start when the user click the button and the function `startAnimation` is fired.

This function add the class `'path'` and the `'path2'` that holds the animations to the elements `'loadingString'` and `'loadingString2'`.

When the last animation ends, there is an event listener to remove the class with the effects and also to display the button that fired the animation.

````html
<script>
var loadingAnimation = document.getElementById('loadingString');
var loadingAnimation2 = document.getElementById('loadingString2');

function startAnimation(){
  //hide the button that started the animation
  document.getElementById('btnLoad').classList.add('hidden');
  
  //add the class 'path' to apply the animation.

  loadingAnimation.classList.remove('hidden');
  loadingAnimation.classList.add('path');
  
  //add the class 'path' to apply the animation #2.
  loadingAnimation2.classList.remove('hidden');
  loadingAnimation2.classList.add('path2'); 
}

//when the animation ends...
loadingAnimation.addEventListener('animationend', () => {
  loadingAnimation.classList.remove('path');
  loadingAnimation.classList.add('hidden');
});  

//when the animation ends
loadingAnimation2.addEventListener('animationend', () => {
  loadingAnimation2.classList.remove('path2');
  loadingAnimation2.classList.add('hidden');
   
  //display again the button
  document.getElementById('btnLoad').classList.remove('hidden');
});

</script>
````

<a href="https://codepen.io/glaucioso/pen/eXxBWV" target="_blank">Live Demo (At CodePen)</a>
