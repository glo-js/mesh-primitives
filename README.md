# mesh-primitives

In this context a "mesh primitive" is a plain JavaScript object which approximates a renderable 2D or 3D mesh. It is not tied to any larger frameworks or engines.

  [<center><img src="http://i.imgur.com/6BKbSZb.png" width="80%" /></center>](http://glo-js.github.io/primitive-torus/)

## modules

- [primitive-sphere](https://www.npmjs.com/package/primitive-sphere)
- [primitive-icosphere](https://www.npmjs.com/package/primitive-icosphere)
- [primitive-torus](https://www.npmjs.com/package/primitive-torus)
- [primitive-quad](https://www.npmjs.com/package/primitive-quad)

## format

The `primitive-*` modules are tailored for rendering purposes (lighting, texturing, etc). Often, they are often not numerically robust.

They provide indexed meshes with counter-clockwise triangles. The returned object has the following structure:

```
{
  positions: [ [x, y, z], [x, y, z], ... ],
  cells: [ [a, b, c], [a, b, c], ... ],
  uvs: [ [u, v], [u, v], ... ],
  normals: [ [x, y, z], [x, y, z], ... ]
}
```

# other mesh modules

There are a number of other generalized mesh modules on npm. Some of them are numerically robust, and others are more useful for demo purposes. These general purpose meshes are often referred to as *simplicial complexes*.

The positions are not always indexed, and may not provide `uvs` or `normals`. They don't always represent 2D or 3D meshes.

Examples:

- [icosphere](https://www.npmjs.com/package/icosphere)
- [sphere-mesh](https://www.npmjs.com/package/sphere-mesh)
- [cube-mesh](https://www.npmjs.com/package/cube-mesh)
- [bunny](https://www.npmjs.com/package/bunny)
- [snowden](https://www.npmjs.com/package/snowden)

For a larger list of generalized meshes, and utilities for manipulating these structures, see [stack.gl/packages](http://stack.gl/packages/#hughsk/icosphere) under the "Geometry" heading.

## License

MIT, see [LICENSE.md](http://github.com/glo-js/mesh-primitives/blob/master/LICENSE.md) for details.
