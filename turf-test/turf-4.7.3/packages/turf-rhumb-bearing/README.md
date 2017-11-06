# @turf/rhumb-bearing

# rhumbBearing

Takes two [points](http://geojson.org/geojson-spec.html#point) and finds the bearing angle between them along a Rhumb line
i.e. the angle measured in degrees start the north line (0 degrees)

**Parameters**

-   `start` **([Geometry](http://geojson.org/geojson-spec.html#geometry) \| [Feature](http://geojson.org/geojson-spec.html#feature-objects)&lt;[Point](http://geojson.org/geojson-spec.html#point)> | [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)>)** starting Point
-   `end` **([Geometry](http://geojson.org/geojson-spec.html#geometry) \| [Feature](http://geojson.org/geojson-spec.html#feature-objects)&lt;[Point](http://geojson.org/geojson-spec.html#point)> | [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)>)** ending Point
-   `final` **\[[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)]** calculates the final bearing if true (optional, default `false`)

**Examples**

```javascript
var point1 = turf.point([-75.343, 39.984], {"marker-color": "#F00"});
var point2 = turf.point([-75.534, 39.123], {"marker-color": "#00F"});

var bearing = turf.rhumbBearing(point1, point2);

//addToMap
var addToMap = [point1, point2]
point1.properties.bearing = bearing
point2.properties.bearing = bearing
```

Returns **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** bearing from north in decimal degrees, between -180 and 180 degrees (positive clockwise)

<!-- This file is automatically generated. Please don't edit it directly:
if you find an error, edit the source file (likely index.js), and re-run
./scripts/generate-readmes in the turf project. -->

---

This module is part of the [Turfjs project](http://turfjs.org/), an open source
module collection dedicated to geographic algorithms. It is maintained in the
[Turfjs/turf](https://github.com/Turfjs/turf) repository, where you can create
PRs and issues.

### Installation

Install this module individually:

```sh
$ npm install @turf/rhumb-bearing
```

Or install the Turf module that includes it as a function:

```sh
$ npm install @turf/turf
```