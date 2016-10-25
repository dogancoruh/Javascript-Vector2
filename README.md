# Javascript-Vector2

Javascript Vector2 support class for 2D vector operations. This library can be used to store vector's x and y data as an instance or to make vector operations like add, subtract, rotate, determining angle between two vectors as a static class.

Features
--------
* 2D vector operations like add, subtract, etc.
* Calculate distance between two vectors/points.
* Rotate a vector by degree or radians.
* Calculate angle between two vectors for signed, unsigned and 360 degree value.
* Sort vectors/points by angle
* Calculate center of points
* Calculate total area of points

Usage
-----

Create a vector
```javascript
var v = new Vector2(5, 3); // x, y
var v = Vector2.empty; // 0, 0
```
Add, Subtract vectors
```javascript
var v1 = new Vector2(5, 3);
var v2 = new Vector2(4, 4);
var v3 = Vector2.add(v1, v2);
var v4 = Vector2.subtract(v1, v2);
```
Multiply, Divide by scalar
```javascript
var v = new Vector2(4, 4);
var vM = Vector2.multiply(v, 3); //12, 12
var vD = Vector2.divide(v, 2); // 2, 2
```
Inverse
```javascript
var v = new Vector2(4, 4);
var vI = Vector2.inverse(v); // -4, -4
```
Set Length
```javascript
var v = new Vector2(5, 3);
var vL = Vector2.setLength(v, 5); // result is same direction, different size
```
isZeroVector
```javascript
var v = new Vector2(5, 3);
if (Vector2.isZeroVector(v))
  console.info("zero vector!");
else
  console.info("not zero vector");
```

magnitude
Gives length of vector
var v = new Vector2(5, 3);
var l = Vector2.magnitude(v);

normalize
Normalizes vector to unit vector (sets its length to 1)
var v = new Vector2(5, 3);
var vN = Vector2.normalize(v);

dot
Gives dot product of two vectors
var v1 = new Vector(7, 2);
var v2 = new Vector(3, 5);
var dot = Vector2.dot(v1, v2);

cross
Gives cross product of two vectors
var v1 = new Vector(7, 2);
var v2 = new Vector(3, 5);
var cross = Vector2.cross(v1, v2);

distance
Gives distance between two vector positions
var v1 = new Vector2(6, 6);
var v2 = new Vector2(2, 4);
var distance = Vector2.distance(v1, v2);

rotateRadian
Rotates vector by radians
var v = new Vector2(4, 4);
var vR = Vector2.rotateRadian(Math.PI / 2);

rotateDegree
Rotates vector by degrees
var v = new Vector2(5, 0);
var vD = Vector2.rotateDegree(90); // rotates 90 degrees in clockwise

angleUnsigned
Gives angle between two vectors without sign in 180 degrees
var v1 = new Vector2(-3, 4);
var v2 = new Vector2(5, 3);
var angle = Vector2.angleUnsigned(v1, v2);

angleSigned
Gives angle between two vector with sign in 180 degrees
var v1 = new Vector2(-3, 4);
var v2 = new Vector2(5, 3);
var angle = Vector2.angleSigned(v1, v2);

angle360
Gives angle between two vector in 360 degreese
var v1 = new Vector2(-3, 4);
var v2 = new Vector2(5, 3);
var angle = Vector2.angle360(v1, v2);

isEqual
Returns true if two given vectors are equal for x an y values
var v1 = new Vector2(3, 3);
var v2 = new Vector2(3, 3);
if (Vector2.equals(v1, v2))
  console.info("equals!");
else
  console.info("not equal");

centerOfPoints
Gets center point of given vector points
var points = new Array();
points.add(new Vector2(10, 10));
points.add(new Vector2(10, 15));
points.add(new Vector2(4, 5));
points.add(new Vector2(8, 7));
var vCenter = Vector2.centerOfPoints(points);

sortPointsByAngle
Sorts points by starting from X axis
var points = new Array();
points.add(new Vector2(10, 10));
points.add(new Vector2(10, 15));
points.add(new Vector2(4, 5));
points.add(new Vector2(8, 7));
points = points.sortPointsByAngle(points);

areaOfPoints
Get total area that given points take
var points = new Array();
points.add(new Vector2(10, 10));
points.add(new Vector2(10, 15));
points.add(new Vector2(4, 5));
points.add(new Vector2(8, 7));
var areaSize = points.areaOfPoints(points);
