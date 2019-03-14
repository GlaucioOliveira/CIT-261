## Code Topic Fluency 

### DOM
> Manipulation Using createElement, appendChild, insertBefore, removeChild, etc.

DOM stands for **D**ocument **O**bject **M**odel. It's a Model created in a structure similar to a tree. The top of this tree is the **document** object and all elements on the page inherit from it. The picture below demonstrate an example:

<img src="https://www.w3schools.com/js/pic_htmltree.gif" />

The html source for this DOM tree structure is the following:

````html
<html>
<head>
  <title>My title</title>
</head>
<body>
  <a href="http://github.com">My link</a>
  <h1>My header</h1>
</body>
</html>	
````
The elements are added at the DOM even considering the moment when they were inserted on the page. On the node of the element `<body>`, the element `<a>` comes first on the node, before the `<h1>` element because that's how it was written on the source code.

The advantage of this tree structure is that we can add elements inside at any elements (nodes) after or before them,  and even creating new nodes to **parent nodes** (*any node that has a child is a parent node*).
