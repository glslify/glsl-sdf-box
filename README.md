# glsl-sdf-box

[![stable](http://badges.github.io/stability-badges/dist/stable.svg)](http://github.com/badges/stability-badges)

GLSL SDF function for generating a box. Determines the distance between a
point and the surface of a box at the origin.

**[view demo](http://stack.gl/glsl-sdf-box/)**

Originally sourced from
[Modeling with Distance Functions](http://iquilezles.org/www/articles/distfunctions/distfunctions.htm) by
[Iñigo Quílez](http://iquilezles.org/).

## Usage

[![NPM](https://nodei.co/npm/glsl-sdf-box.png)](https://nodei.co/npm/glsl-sdf-box/)

### `float box(vec3 position, vec3 dimensions)`

Returns the signed distanced between `position` and a box at the origin
with a given set of `dimensions`. For example, to draw a 2x2x2 box in a
raytracing shader:

``` glsl
#pragma glslify: box = require('glsl-sdf-box')

vec2 doModel(vec3 p) {
  float dist   = box(p, vec3(2.0));
  float id     = 1.0;

  return vec2(dist, id);
}
```

## Contributing

See [stackgl/contributing](https://github.com/stackgl/contributing) for details.

## License

MIT. See [LICENSE.md](http://github.com/stackgl/glsl-sdf-box/blob/master/LICENSE.md) for details.
