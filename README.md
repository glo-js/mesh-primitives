# mesh-primitives

In this context a "mesh primitive" is a plain JavaScript object which approximates a renderable 2D or 3D mesh. It is not tied to any larger frameworks or engines.

  [<center><img src="http://i.imgur.com/6BKbSZb.png" width="80%" /></center>](http://glo-js.github.io/primitive-torus/)

## modules

- [primitive-sphere](https://www.npmjs.com/package/primitive-sphere)
- [primitive-icosphere](https://www.npmjs.com/package/primitive-icosphere)
- [primitive-torus](https://www.npmjs.com/package/primitive-torus)
- [primitive-quad](https://www.npmjs.com/package/primitive-quad)
- [primitive-cube](https://www.npmjs.com/package/primitive-cube)

## format

The `primitive-*` modules are tailored for rendering purposes (lighting, texturing, etc) and are typically used in prototypes and demos. Often, they are often not numerically robust.

They provide indexed meshes with counter-clockwise triangles. The returned object has the following structure:

```
{
  positions: [ [x, y, z], [x, y, z], ... ],
  cells: [ [a, b, c], [a, b, c], ... ],
  uvs: [ [u, v], [u, v], ... ],
  normals: [ [x, y, z], [x, y, z], ... ]
}
```

# generic mesh modules

##### a.k.a. "simplicial complexes"

There are a number of other generalized mesh modules on npm. Some of them are numerically robust. These general purpose meshes are often referred to as **"simplicial complexes"**.

```
{
  positions: [ [x, y, z], [x, y, z], ... ], // n-dimensional
  cells: [ [a, b, c], [a, b, c], ... ]      // optional
}
```

The positions are not always indexed, and may not provide `uvs` or `normals`. They don't always represent 2D or 3D meshes, and the winding order might not always be consistent.

Examples:

- [icosphere](https://www.npmjs.com/package/icosphere)
- [sphere-mesh](https://www.npmjs.com/package/sphere-mesh)
- [cube-mesh](https://www.npmjs.com/package/cube-mesh)
- [bunny](https://www.npmjs.com/package/bunny)
- [snowden](https://www.npmjs.com/package/snowden)
- [geo-piecering](https://www.npmjs.com/package/geo-piecering)
- [geo-arc](https://www.npmjs.com/package/geo-arc)
- [geo-asterisk](https://www.npmjs.com/package/geo-asterisk)
- [svg-mesh-3d](https://www.npmjs.com/package/svg-mesh-3d)

## manipulation

There are dozens of modules for manipulating these data structures on npm, such as:

- [mesh-combine](https://github.com/hughsk/mesh-combine)
- [merge-vertices](https://github.com/thibauts/merge-vertices/blob/master/index.js)
- [remove-degenerate-cells](https://github.com/thibauts/remove-degenerate-cells)
- [normals](https://github.com/mikolalysenko/normals)
- [convex-hull](https://www.npmjs.com/package/convex-hull)
- [cdt2d](https://www.npmjs.com/package/cdt2d)
- [simplify-path](https://www.npmjs.com/package/simplify-path)

For a larger list of modules, see [stack.gl/packages](http://stack.gl/packages/#hughsk/icosphere) under the "Geometry" heading.

## rendering

There are a variety of modules to facilitate rendering of these 2D and 3D mesh modules.

#### Canvas2D

- [draw-triangles-2d](https://www.npmjs.com/package/draw-triangles-2d)

#### ThreeJS

- [three-simplicial-complex](https://github.com/Jam3/three-simplicial-complex)

#### stackgl

- [mesh-viewer](https://www.npmjs.com/package/mesh-viewer)
- [gl-geometry](https://www.npmjs.com/package/gl-geometry)

## License

MIT, see [LICENSE.md](http://github.com/glo-js/mesh-primitives/blob/master/LICENSE.md) for details.
