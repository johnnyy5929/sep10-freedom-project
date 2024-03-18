# Tool Learning Log

Tool: **Aframe**

---

X/X/X:
LL1

X/X/X:
LL2

### How to install Aframe
https://aframe.io/docs/1.5.0/introduction/javascript-events-dom-apis.html
````
<head>
  <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
</head>
````



#### Learning the shapes

````
<html>
  <head>
    <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
      <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9"></a-box>
      <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
      <a-cylinder position="1 0.75 -3" radius="0.5" height="1.5" color="#FFC65D"></a-cylinder>
      <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>
      <a-sky color="#ECECEC"></a-sky>
    </a-scene>
  </body>
</html>
````

#### The basic

* I learned how to add a box
````
 <body>
   <a-scene>
      <a-box>
      </a-box>
   </a-scene>
</body>

````

* To change the properties of the shape you can add color, weight, height, depth and more it will look something like
````
 <body>
   <a-scene>
      <a-box color=""
             weight=""
             height=""
             depth="">
      </a-box>
   </a-scene>
</body>

````




https://www.youtube.com/watch?v=K4LEMBjaV9E&list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV&index=6

Parent-Child Relationships
When A-Frame entities are nested in parent-child relationships, so are their three.js objects. For example, take this A-Frame scene:

````
<a-scene>
  <a-box>
    <a-sphere></a-sphere>
    <a-light></a-light>
  </a-box>
</a-scene>
````


3/17/24
LL3


https://www.youtube.com/watch?v=K4LEMBjaV9E&list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV&index=6
https://aframe.io/docs/1.5.0/introduction/javascript-events-dom-apis.html

````
