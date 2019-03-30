## Code Topic Fluency 

### CSS3 Transitions
> Designing, Defining, and Triggering CSS3 Transitions without Custom Libraries.

With the CSS Transition, we are able to trigger transitions of style properties of an element from one start position (or size) to an end position (or size). We are able with this functionality also to control the length that this transition happens and also a delay to the animation to occurr.

In the code below there is an example of a transition of a transform property to rotate a fan image, to simulate it to be spinning. The start value is defined at the #load-img style and the end value is defined at the .load-img2 style. 

The duration for this animation is defined on the **transition-duration** property with the value of 100 seconds. There is also a delay for the animation defined with the **transition-delay** property with the value of 0.2 secoonds.

````html
<style>
.load-img2 {
  transform: rotate(100.0turn);
}

#load-img{
  width:32px;
  height:32px;
  
  transition-property: transform;
  transition-duration: 100s;
  transition-delay: 0.5s;
  
  display:block;
  margin-bottom:5px;
}
</style>

<div>
  <h3>Fan</h3>
   <img id="load-img" src="http://goliveira.com/byui/resources/ventilating-fan.png" />

<button onclick="TurnOn();">Turn ON</button>
<button onclick="TurnOff();">Tur OFF</button>
</div>
````

<a href="https://codepen.io/glaucioso/pen/Ladqyr" target="_blank">Live Demo (At CodePen)</a>
