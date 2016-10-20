# Javascript-Vector2

Javascript Vector2 support class for 2D vector operations. This library can be used to store vector's x and y data as an instance or to make vector operations like add, subtract, rotate, determining angle between two vectors as a static class.

Features
--------
* 2D vector operations like add, subtract, etc.
* Calculate distance between two vectors/points.
* Rotate a vector by degree or radians.
* Calculate angle between two vectors for signed, unsigned and 360 degree value.

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
