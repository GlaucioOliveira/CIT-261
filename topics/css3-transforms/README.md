## Code Topic Fluency 

### CSS3 Transforms
> Designing, Defining, and Triggering CSS3 Transforms without Custom Libraries.

With the CSS Transform we are able to apply effects to elements that enalbe us to rotate, scale, translate and skew them. 

In the code below there is the continuation of the example used on the [Transition Topic](../css3-transitions/README.md), but now adding Transform effects.
On the example below there is an animation to rotate the #demo div when the :hover event is triggered (with the mouse hover the #demo div). We are also able to include Transform effects on the **transition-property** as demonstrated on this example.

````html
<style>
  #demo {
  font-size: 30px;
  transition-property: font-size, color, padding, border, transform;
  transition-duration: 0.8s;
  transition-delay: 0.2s;
  color:black;
  cursor:pointer;
  border: 1px solid white;
  transform: rotate(1deg);
  width:500px;
}

#demo:hover {
  font-size: 32px;
  color:darkblue;
  padding:10px;
  border:10px solid green;
  transform: rotate(-5deg);
}
</style>

<div id="demo">
  CSS Transform Demo
</div>
````

<a href="https://codepen.io/glaucioso/pen/LadaEa" target="_blank">Live Demo (At CodePen)</a>
