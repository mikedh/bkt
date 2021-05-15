# bkt
### Badly Known Text

An attempt to encode 2D or 3D curves with a simple JSON schema. WKT and WKB are explicitly 2D, and also generally only have line primitives, not circular arcs or bezier curves. DXF files 

- All elements can have `(n, 2)` (assumed to be on X-Y plane) or `(n, 3)` vertices.
- All elements can specify an `(4, 4)` or `(3, 3)` homogenous transformation matrix.
- All elements populate the `kind` field.


### Entities

All entities can have a `matrix`, and have a `kind` field defined. 

#### LineString
- `(n, 2)` or `(n, 3)` vertices

#### Circle
- `(3, 2)` or `(3, 3)` control points for a 3-point arc
- `closed` boolean flag indicating circular arc vs closed circle.

