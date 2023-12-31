# VizLib

VizLib is a JavaScript library for canvas-based graphics and geometry functions. It provides a collection of utility functions for working with HTML5 Canvas, including functions for manipulating canvas size, drawing shapes, generating random values, and performing various geometric calculations.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Functions](#functions)
- [Examples](#examples)
- [License](#license)

## Installation

You can install VizLib using npm:

```bash
npm install vizlib
```

## Usage

To use VizLib in your project, you need to include it and have an HTML5 canvas element (`<canvas>`) with the appropriate context (`ctx`) set up in your project. Here's how you can get started:

```javascript
const canvas = document.getElementById("myCanvas");
const ctx = canvas.getContext("2d");

// Import VizLib
const vizlib = require("vizlib");

// Set the canvas size to fit the window
vizlib.maxify();

// Draw a circle
vizlib.drawCircle(vizlib.middleX(), vizlib.middleY(), 30, "blue", 2);

// Generate a random color
const randomFill = vizlib.randomColor();
console.log(randomFill);
```

## Functions

VizLib provides a wide range of functions organized into different categories:

### Canvas Size Functions

- `maxify(cutBy = 5.5)`: Sets the canvas width and height to be 10 pixels less than the window width and height, respectively.
- `middleX()`: Returns the x-coordinate of the canvas center.
- `middleY()`: Returns the y-coordinate of the canvas center.
- `endX()`: Returns the x-coordinate at the end of the canvas.
- `endY()`: Returns the y-coordinate at the end of the canvas.
- `fillCanvas(color = "white")`: Fills the entire canvas with the specified color.
- `clearCanvas()`: Clears the entire canvas.
- `drawHorizontal(y = middleY(), color = "grey")`: Draws a horizontal axis line on the canvas.
- `drawVertical(x = middleX(), color = "grey")`: Draws a vertical axis line on the canvas.
- `drawAxes(color = "grey")`: Draws both horizontal and vertical axes on the canvas.
- `getAcceptableX(radius)`: Returns an acceptable x-coordinate for a circle with the given radius.
- `getAcceptableY(radius)`: Returns an acceptable y-coordinate for a circle with the given radius.

### Randomization Functions

- `randRange(min, max)`: Generates a random rational number between `min` (inclusive) and `max` (exclusive).
- `randInt(min, max)`: Generates a random integer between `min` (inclusive) and `max` (exclusive).
- `randItem(arr)`: Returns a random element from an array.
- `randomSign()`: Returns a random sign value (-1 or 1).
- `randomColor(opacity = 1)`: Generates a random RGBA color with optional opacity.
- `positive(number)`: Returns the absolute value of a number.
- `negative(number)`: Returns the negation of a number.
- `absDiff(x1, x2)`: Computes the absolute difference between two numbers.

### Geometric and Distance Functions

- `getDistance(x1, y1, x2, y2)`: Calculates the distance between two points (x1, y1) and (x2, y2).
- `isPointInsideCircle(x1, y1, x2, y2, r2)`: Checks if a point (x1, y1) is inside a circle with center (x2, y2) and radius `r2`.
- `isPointInsideSquare(x1, y1, x2, y2, size2)`: Checks if a point (x1, y1) is inside a square with top-left corner (x2, y2) and side length `size2`.
- `isPointInsideRectangle(x1, y1, x2, y2, length2, breadth2)`: Checks if a point (x1, y1) is inside a rectangle with top-left corner (x2, y2), length `length2`, and breadth `breadth2`.
- `getDegreeFromRadian(rad)`: Converts an angle from radians to degrees.

### Object and Array Functions

- `updateArray(arr)`: Calls the `update` method on each object in an array.
- `updateObject(obj)`: Calls the `update` method on each object property in an object.
- `arrayOfObjects(n, clas)`: Generates an array of `n` objects of the specified class.

### Complex Geometry Functions

- `newX(x, y, r, theta = 0)`: Calculates the new x-coordinate

after moving `r` units at an angle of `theta` from the point (x, y).

- `newY(x, y, r, theta = 0)`: Calculates the new y-coordinate after moving `r` units at an angle of `theta` from the point (x, y).
- `drawLineSegment(x1, y1, x2, y2, color, lineWidth)`: Draws a line segment between two points on the canvas.

### Miscellaneous Functions

- `giveCoordinatesArray(size, gap)`: Generates an array of coordinates that fill up the entire canvas with a specified size and gap.
- `getQuadrant(x1, y1, x2, y2)`: Determines the quadrant of a point (x2, y2) with respect to an origin point (x1, y1) in the canvas coordinate system.
- `getActualTheta(theta, quadrant)`: Converts an angle in radians to its actual value in the range [0, 2π] based on the quadrant.
- `getAngle(x1, y1, x2, y2)`: Calculates the angle in radians between two points (x1, y1) and (x2, y2) with (x1, y1) as the origin.
- `getAngleInDegrees(x1, y1, x2, y2)`: Calculates the angle in degrees between two points (x1, y1) and (x2, y2) with (x1, y1) as the origin.
- `hypot(x, y)`: Computes the length of the hypotenuse of a right triangle with legs of lengths `x` and `y`.

## License

VizLib is licensed under the [MIT License](LICENSE).

---

Feel free to customize this README to fit your project's specific needs. If you have any additional information or usage examples to include, please do so.
