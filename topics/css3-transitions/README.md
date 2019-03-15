## Code Topic Fluency 

### CSS3 Transitions
> Designing, Defining, and Triggering CSS3 Transitions without Custom Libraries.

With the CSS Transition, we are able to trigger transitions of style properties of an element from one start position (or size) to an end position (or size). We are able with this functionality also to control the length that this transition happens and also a delay to the animation to occurr.

In the code below there is an example of a transition of the properties (font-size, color, padding and border). The start value is defined at the #demo style and the end value is defined at the #demo:hover style. 

The duration for this animation is defined on the **transition-duration** property with the value of 0.8 seconds. There is also a delay for the animation defined with the **transition-delay** property with the value of 0.2 secoonds.

````html
<style>
  #demo {
  font-size: 30px;
  transition-property: font-size, color, padding, border;
  transition-duration: 0.8s;
  transition-delay: 0.2s;
  color:black;
  cursor:pointer;
  border: 1px solid white;
}

#demo:hover {
  font-size: 32px;
  color:darkblue;
  padding:10px;
  border:10px solid green;
}
</style>

<div id="demo">
  CSS Transition Demo
</div>
````

<a href="https://codepen.io/glaucioso/pen/Ladqyr" target="_blank">Live Demo (At CodePen)</a>
