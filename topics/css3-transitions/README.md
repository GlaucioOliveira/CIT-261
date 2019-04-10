## Code Topic Fluency 

### CSS3 Transitions
> Designing, Defining, and Triggering CSS3 Transitions without Custom Libraries.

With the CSS Transition, we are able to trigger transitions of style properties of an element from one start position (or size) to an end position (or size). We are able with this functionality also to control the length that this transition happens and also a delay to the animation to occurr.

In the code below there is an example of a transition of a transform property to rotate a fan image, to simulate it to be spinning. The start value is defined at the #load-img style and the end value is defined at the .load-img2 style. 

The duration for this animation is defined on the **transition-duration** property with the value of 100 seconds. There is also a delay for the animation defined with the **transition-delay** property with the value of 0.2 secoonds.

````html
<style>
ul{
  background-color:greenyellow;
  display:block;
  overflow:auto;
  padding-bottom:10px;
  height:32px;
}

li {
  transition-property: border, padding;
  float:left;
  padding: 10px;
  list-style-type:none;
  color: red;
  cursor:pointer;
  
}

li:hover {
  transition-property: border, color;
  border-bottom: 5px solid darkgreen;
  transition-duration: 0.4s;
  color:white;
}
</style>

<h1>Demo Company </h1>

<ul>
  <li>Home</li>
  <li>Our History</li>
  <li>Clients</li>
  <li>About Us</li>
</ul>
````

<a href="https://codepen.io/glaucioso/pen/eoWOgM" target="_blank">Live Demo (At CodePen)</a>
