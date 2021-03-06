# @turf/rhumb-destination

# rhumbDestination

Returns the destination [Point](http://geojson.org/geojson-spec.html#point) having travelled the given distance along a Rhumb line from the
origin Point with the (constant) given bearing.

**Parameters**

-   `origin` **([Geometry](http://geojson.org/geojson-spec.html#geometry) \| [Feature](http://geojson.org/geojson-spec.html#feature-objects)&lt;[Point](http://geojson.org/geojson-spec.html#point)> | [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)>)** starting point
-   `distance` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** distance from the starting point
-   `bearing` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** constant bearing angle ranging from -180 to 180 degrees from north
-   `units` **\[[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)]** miles, kilometers, degrees, or radians (optional, default `kilometers`)

**Examples**

```javascript
var point = turf.point([-75.343, 39.984], {"marker-color": "F00"});
var distance = 50;
var bearing = 90;
var units = 'miles';

var destination = turf.rhumbDestination(point, distance, bearing, units);

//addToMap
var addToMap = [point, destination]
destination.properties['marker-color'] = '#00F';
```

Returns **[Feature](http://geojson.org/geojson-spec.html#feature-objects)&lt;[Point](http://geojson.org/geojson-spec.html#point)>** Destination point.

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
$ npm install @turf/rhumb-destination
```

Or install the Turf module that includes it as a function:

```sh
$ npm install @turf/turf
```
