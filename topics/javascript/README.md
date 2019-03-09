## Code Topic Fluency 

### JavaScript
> Loops, Conditional Statements, Functions, Variables, Parameters, Arrays, Associative Arrays.

Note: All the examples below to be executed needs to be inside a HTML page structure and inside the script tag (`<script>`).

#### Variables
> Variables are containers where data can be stored. In the code below, the 'teacherName' is a variable. JavaScript recognizes this 'teacherName' as a variable because of the special keyword *var* before the 'teacherName'. 
The equal sign (=) is used to assign the value 'Gláucio Oliveira', to the variable.

```html
<script>
  //example of a variable
  var teacherName = "Gláucio Oliveira";
  alert(teacherName); //a message will be displayed with the value of the teacherName variable
</script>
```


#### Arrays
> To store more then one information in a single variable we can make use of arrays. Arrays works just like variables in JavaScript. The difference is that we need to specify multiple values to it, we do it using the [ ] characters.


```html
...
<script>
  //example of an array of foods;
  var Foods = ["Apple","Banana","Coconut"];
  alert(Foods[0]); //a message will be displayed with the value of the first fruit on the Array Foods.
</script>
```

#### Associative Arrays
> In the example above, when we are accessing the first item (fruit) on the Array 'Foods', with the [0] index, we are acessing something called *associative array*. We can only access arrays by their position in the Array. This is a zero based array, so the first item is in the position 0. and the last one is 2. (0 = Apple, 1 = Banana, 2 = Coconut). 


#### Functions and Parameters
> A function is a block of code (inside a { } brackets) that execute a particular task. It needs to be inside a function declaration (or header) that it is composed by the *function* keyword, next to the name of the function and the ( ) parentheses. To pass parameters, we only need to name then inside the ( ) parentheses with their names. 

In the example below there a function (doTheMath) that multiplies two values passed to it through the parameters (param1 and param2). Those parameters are acessible only inside the scope of the function.


```html
...
<script>
  function doTheMath(param1, param2){
    return param1 * param2; //with the *return* keyword we assign the result of this function to where it was executed.
  }
  
  var result = doTheMath(10, 5); //calls the function declared above passing the values 10 and 5 as parameters.
</script>
```

#### Conditional Statements (if, else)
> With conditional statements we are able to execute specific blocks of codes, if a condition is reached. 
  in the function *doTheMath* below, before doing the Math operation it checks to see if the values passed in the parameters are valid numbers by calling the JavaScript function *isNaN*. If it's a valid number the *isNaN* returns false, otherwise returns true.
The function *doTheMath* will only be executed if both parameters are valid numbers.

```html
...
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
</script>
```
