## Code Topic Fluency 

### JavaScript
> Loops, Conditional Statements, Functions, Variables, Parameters, Arrays, Associative Arrays.

Note: All the examples below to be executed needs to be inside a HTML page structure and inside the script tag (<script>).

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
  //example of a array of foods;
  var Foods = ["Apple","Banana","Coconut"];
  alert(Foods[0]); //a message will be displayed with the value of the first fruit on the Array Foods.
</script>
```

#### Associative Arrays
> In the example above, when we are accessing the first item (fruit) on the Array 'Foods', with the [0] index, we are acessing something called *associative array*. We can only access arrays by their position in the Array. This is a zero based array, so the first item is in the position 0. and the last one is 2. (0 = Apple, 1 = Banana, 2 = Coconut). 
