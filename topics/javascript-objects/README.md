## Code Topic Fluency 

### JavaScript Objects
> Object Creation, Functions, Inheritance, Properties, Methods, Instantiation.

To represent things of the real world (like car, house, food, etc...) into programming language that are Object Oriented (POO) we can create classes that has properties and methods related to those things. An Object is an instance of this class. JavaScript is not an Object Oriented Language, but <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes" target="_blank">recently it added a keyword named **class**</a> (TypeScript is what leads JavaScript more close to a POO with a transpilation process) and it's prototype-based (<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain" target="_blank">definition here</a>).

In the example below there is the definition of a class named 'Rectangle' with properties and a method. and the variable rec1 creates an instance of this class. All the bahavior from the class are now accessible from this variable/object.

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
