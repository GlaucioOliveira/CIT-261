## Code Topic Fluency 

### JavaScript
> Loops, Conditional Statements, Functions, Variables, Parameters, Arrays, Associative Arrays.

Note: All the examples below to be executed needs to be inside a HTML page structure and inside the script tag (`<script>`).

#### Variables
Variables are containers where data can be stored. In the code below, the 'teacherName' is a variable. JavaScript recognizes this `teacherName` container as a variable because of the special keyword *var* before the `teacherName`. 
The equal sign (=) is used to assign the value 'Gláucio Oliveira' to the variable.

```html
<script>
  //example of a variable
  var teacherName = "Gláucio Oliveira";
  document.write(teacherName); //display the value of the teacherName variable.
</script>
```
<a href="https://codepen.io/glaucioso/pen/EMXyZo" target="_blank">Live Demo (at CodePen)</a>

#### Arrays
To store more then one information in a single variable we can make use of arrays. Arrays works just like variables in JavaScript. The difference is that we need to specify multiple values to it, we do it using the [ ] square brackets.


```html
<script>
  //example of an array containg a list of foods;
  var Foods = ["Apple","Banana","Coconut"];
  document.write(Foods[0]); //Display the value of the first fruit on the Array Foods.
</script>
```

#### Associative Arrays
In the example above, when we are accessing the first item (fruit) on the Array 'Foods', with the [0] index, we are acessing something called *associative array*. We can only access arrays by their position in the Array. This is a zero based array, so the first item is in the position 0. and the last one is 2. (0 = Apple, 1 = Banana, 2 = Coconut). 

<a href="https://codepen.io/glaucioso/pen/mowEMY" target="_blank">Live Demo (at CodePen)</a>

#### Functions and Parameters
A function is a block of code (inside a { } curly braces) that execute a particular task. It needs to be inside a function declaration (or header) that it's composed by the *function* keyword, next to the name of the function and the ( ) parentheses. To pass parameters, we only need to name them inside the ( ) parentheses, separated by a comma when there is more then one. 

In the example below there a function (doTheMath) that multiplies two values passed to it through the parameters (param1 and param2). Those parameters are acessible only inside the scope of the function (outside the doTheMath function those values are to accessible).


```html
<script>
  function doTheMath(param1, param2){
    return param1 * param2;
  }
  
  var result = doTheMath(10, 5); //calls the function declared above passing the values 10 and 5 as parameters.
  
  document.write(result); //display the result.
</script>
```
<a href="https://codepen.io/glaucioso/pen/JzJKrB" target="_blank">Live Demo (at CodePen)</a>


#### Conditional Statements (If, Else)
With conditional statements we are able to execute specific blocks of codes, if a condition is reached. In the function *doTheMath* below, before doing the Math operation it checks to see if the values passed in the parameters are valid numbers by calling the JavaScript function *isNaN*. If it's a valid number the *isNaN* returns false, otherwise returns true.
The function *doTheMath* will only be executed if both parameters are valid numbers.

```html
<script>
  function doTheMath(param1, param2){
    if(isNaN(param1) == true) {
      return -1; 
    }
    else if (isNaN(param2) == true) {
      return -1;
    }
  
    //If param1 and param2 are valid numbers, then do the Math!
    return param1 * param2;
  }
  
  var result = doTheMath(10, 5);
  document.write(result);
</script>
```
<a href="https://codepen.io/glaucioso/pen/vPZKWM" target="_blank">Live Demo (at CodePen)</a>


#### Loops (For, While)
Loops are ways to excute a block of code as long as a condition is true. 

```html
<script>
  for(var i = 0; i <= 5; i++){
      //do something until i == 5
     document.write("(for loop) => i = " + i + "<br/>");
    }
                        
var counter = 4;                   
  while (counter > 0){ //loop until counter is higher then 0.
   counter = counter - 1;
    document.write("(while loop) => counter = " + counter + "<br/>");
  }
</script>
```
<a href="https://codepen.io/glaucioso/pen/rRGWjb" target="_blank">Live Demo (at CodePen)</a>


#### Demo Application

Below there is a Live Demo for an Questionary application, using some of the principles learned at this code Topic.

<a href="https://codepen.io/glaucioso/pen/dLWbeb" target="_blank">Live Demo (at CodePen)</a>
