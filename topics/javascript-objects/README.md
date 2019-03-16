## Code Topic Fluency 

### JavaScript Objects
> Object Creation, Functions, Inheritance, Properties, Methods, Instantiation.

To represent things of the real world (like a car, a house, a food, etc...) into a programming language that is [Object Oriented (OOP)](https://en.wikipedia.org/wiki/Object-oriented_programming) we can create classes that got properties and methods related to those real world objects. By definition, an object is an instance of this class.

JavaScript is not an Object Oriented Language, but <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes" target="_blank">recently it added a keyword named **class**</a> (TypeScript is what leads JavaScript more close to a POO with a transpilation process). JavaScript is prototype-based (<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain" target="_blank">definition here</a>).

In the example below there is the definition of a class named 'Rectangle' with properties (width, height), a constructor (a type of function that is executed on the creation of the object) and two functions (calcArea and displaySize). 
The variable rec1 creates an instance of this class (so rec1 becames a Rectangle object) and all the bahavior from the class are now accessible at this variable..

```html
<script>
  class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }

  calcArea(){
    return rec1.width * rec1.height;
  }
    
 displaySize(){
   document.write(rec1.width + " X " + rec1.height + " Area => " + this.calcArea());
 }

}
  
 var rec1 = new Rectangle(100, 200);
 rec1.displaySize();
</script>
```

<a href="https://codepen.io/glaucioso/pen/OqOvYd" target="_blank">Live Demo (at CodePen)</a>
