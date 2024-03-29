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

Link:
https://www.youtube.com/watch?v=K4LEMBjaV9E&list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV&index=6
https://aframe.io/docs/1.5.0/introduction/javascript-events-dom-apis.html



How to add sky:
````
<a-scene>
  <a-assets>
    <img id="sky" src="sky.png">
  </a-assets>
  <a-sky src="#sky"></a-sky>
</a-scene>
````


````
<a-sky color="#6EBAA7"></a-sky>
````

About how the camera: 

````
<a-scene>
  <a-box></a-box>
  <a-camera></a-camera>
</a-scene>
````
````
<!-- Place camera at ground level (will be overridden by VR devices) -->
<a-camera position="0 0 0"></a-camera>
````

````
<a-entity id="rig" position="25 10 0">
  <a-camera id="camera"></a-camera>
</a-entity>
````
How to add links:
````
<a-scene>
  <a-assets>
    <img id="my-image" src="image.png">
  </a-assets>

  <!-- Using the asset management system. -->
  <a-image src="#my-image"></a-image>

  <!-- Defining the URL inline. Not recommended but more comfortable for web developers. -->
  <a-image src="another-image.png"></a-image>
</a-scene>
````

different shapes:
````
<a-entity geometry="primitive: box; width: 1; height: 1; depth: 1"></a-entity>
````
````
<a-entity geometry="primitive: circle; radius: 1" material="side: double"></a-entity>
````
````
<a-entity geometry="primitive: cone; radiusBottom: 1; radiusTop: 0.1"></a-entity>
````
````
<a-entity geometry="primitive: cylinder; height: 3; radius: 2"></a-entity>
````
````
<a-entity geometry="primitive: cylinder; openEnded: true" material="side: double"></a-entity>
````
````
<a-entity geometry="primitive: cylinder; openEnded: true; thetaLength: 180"
          material="side: double"></a-entity>
````
````
<a-entity geometry="primitive: dodecahedron; radius: 2"></a-entity>
````
````
<a-entity geometry="primitive: octahedron"></a-entity>
````
````
<a-entity geometry="primitive: icosahedron"></a-entity>
````
````
<a-entity geometry="primitive: plane; height: 10; width: 10" material="side: double"></a-entity>
````
````
<a-entity geometry="primitive: ring; radiusInner: 0.5; radiusOuter: 1"
          material="side: double"></a-entity>
````

Reflection:
````
<a-scene reflection="directionalLight:a-light#dirlight;"></a-scene>
	<a-light id="dirlight" intensity="1" light="castShadow:true;type:directional" position="1 1 1"></a-light>
````

Adding text:
````
<html>
  <head>
    <meta charset="UTF-8">
    <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
      <a-sky color="lightblue"></a-sky>
      <a-text value="ABCあいうえお日本語" font="custom-msdf.json" font-image="custom-msdf.png" negate="false" scale="2 2 1" position="-2 2 -4"></a-text>
    </a-scene>
  </body>
</html>
````


Mixins:
````
<a-scene>
  <a-assets>
    <a-mixin id="red" material="color: red"></a-mixin>
    <a-mixin id="blue" material="color: blue"></a-mixin>
    <a-mixin id="cube" geometry="primitive: box"></a-mixin>
  </a-assets>

  <a-entity mixin="red cube"></a-entity>
  <a-entity mixin="blue cube"></a-entity>
</a-scene>
````


3/24/24

LL4

Learning COMPONENTS


Link:
https://www.youtube.com/watch?v=K4LEMBjaV9E&list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV&index=6
https://aframe.io/docs/1.5.0/introduction/javascript-events-dom-apis.html


anchored:
````
<a-entity id="myBox" anchored="persistent: true" geometry="primitive: box" material="color: red"></a-entity>
````

animation: chnages/moves shapes and stuff

````
<a-box position="-1 1.6 -5" animation="property: position; to: 1 8 -10; dur: 2000; easing: linear; loop: true" color="tomato"></a-box>
````

````
<a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="5 0 0" color="mediumseagreen"></a-sphere>
</a-entity>
````
fog:
````
<a-scene fog="type: linear; color: #AAA"></a-scene>
````

hand-controls:
````
<a-entity id="leftHand" hand-controls="hand: left; handModelStyle: lowPoly; color: #ffcccc"></a-entity>
<a-entity id="rightHand" hand-controls="hand: right; handModelStyle: lowPoly; color: #ffcccc"></a-entity>
````

hand-tracking-controls:
````
<a-entity id="leftHand" hand-tracking-controls="hand: left;"></a-entity>
<a-entity id="rightHand" hand-tracking-controls="hand: right;"></a-entity>
````


hand-tracking-grab-controls: 
````
<a-entity id="leftHand" hand-tracking-grab-controls="hand: left;"></a-entity>
<a-entity id="rightHand" hand-tracking-grab-controls="hand: right;"></a-entity>
````

These codes are to interact with everything.

laser-controls:
````
<a-entity laser-controls="hand: left"></a-entity>
````
real-world-meshing:
````
<a-scene real-world-meshing></a-scene>
````

3/25/24

LL5


Trying more animation and with different shapes

````
<html>
  <head>
    <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
      <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9"></a-box>
      <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
      <a-cylinder position="-1 1.5 -3" radius="0.5" height="0.9" color="#FFC65D"></a-cylinder>
      <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>
      <a-sky color="#ECECEC"></a-sky>
      <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="5 0 0" color="mediumseagreen"></a-sphere>
</a-entity>
      <a-box position="-1 0.6 -5" animation="property: position; to: 1 0.6 -10; dur: 2000; easing: linear; " color="tomato"></a-box>
<a-cylinder position="-1 1.6 -5" height="2" radius="0.25"  animation="property: position; to: 1 1.6 -10; dur: 2000; easing: linear; " color="tomato"></a-cylinder>
      
    </a-scene>
  </body>
</html>
````

![hi](hi.png)
````
<html>
  <head>
    <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
      <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9"></a-box>
      <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
      <a-cylinder position="-1 1.5 -3" radius="0.5" height="0.9" color="#FFC65D"></a-cylinder>
      <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>
      <a-sky color="#ECECEC"></a-sky>
      <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="5 0 0" color="mediumseagreen"></a-sphere>
</a-entity>
      <a-box position="-1 0.6 -5" animation="property: position; to: 1 0.6 -10; dur: 2000; easing: linear; " color="tomato"></a-box>
<a-cylinder position="-1 1.6 -5" height="2" radius="0.25"  animation="property: position; to: 1 1.6 -10; dur: 2000; easing: linear; " color="tomato"></a-cylinder>
           <a-box position="-2 0.6 -5" animation="property: position; to: -1.5 0.6 -10; dur: 2000; easing: linear; " color="tomato"></a-box>
<a-cylinder position="-2 1.6 -5" height="2" radius="0.25"  animation="property: position; to: -1.5 1.6 -10; dur: 2000; easing: linear; " color="tomato"></a-cylinder>
      
    </a-scene>
  </body>
</html>
````


