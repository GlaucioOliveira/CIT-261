## Code Topic Fluency 

### CSS Class Properties Using JavaScript
> How to manipulate CSS Class Properties Using JavaScript.

With JavaScript we can manipulate any Object/Element inside the DOM strucutre of a Page. We can change it's behavior and also it's style. We only need to grab the Object/Element (using the function **getElementById**) or a list of Objects/Elements (using the function **getElementsByClassName**) and them apply the change that we want for it.

With the code below, there is a function called **toggleClass** to help with change of classes (toggling them) on the element (div) with the id 'element'. the **toggle** function show/hide the specified class on the parameter.

````html
<script>
  function toggleClass(className){
  document.getElementById("container").classList.toggle(className);
}
</script>

<div id="container" class="">
Hello There. Try to play with the buttons below.
</div>

<br/>

<div>
<button onclick="toggleClass('container-borders')">Toogle Borders</button>
<button onclick="toggleClass('container-fonts')">Toogle Font</button>
  <button onclick="toggleClass('container-colors')">Toogle Colors</button>
</div>
````

The complete code with the code of the classes are on the link below:

<a href="https://codepen.io/glaucioso/pen/BbJbWJ" target="_blank">Live Demo (at CodePen)
