# Appendix D - Vectorworks Object Types and Subtypes

The numeric types in the table below are useful for identifying what type of object is referenced by a handle. The function [VS:GetTypeN](h) will return one of these numeric types. The Criteria values in the table below are used in search criteria statements. They are used along with the criteria *T=* to search for objects of a specific type. For example, the following statement will count the number of rectangles in the active document:

```python
Message( Count(T=RECT) );
```

## Object Types

| Object | Type | Criteria Type Selector | Criteria Example |
|--------|------|------------------------|------------------|
| Line | 2 | LINE | T=LINE |
| Rectangle | 3 | RECT | T=RECT |
| Oval | 4 | OVAL | T=OVAL |
| Polygon | 5 | POLY | T=POLY |
| Arc | 6 | ARC | T=ARC |
| Freehand | 8 | FHAND | T=FHAND |
| 3D Locus | 9 | LOCUS3D | T=LOCUS3D |
| Text | 10 | TEXT | T=TEXT |
| Group | 11 | GROUP | T=GROUP |
| Rounded rectangle | 13 | RRECT | T=RRECT |
| Bitmap Image | 14 | BITMAP | T=BITMAP |
| Symbol instance | 15 | SYMBOL | T=SYMBOL |
| Symbol Definition (1) | 16 |  |  |
| 2D Locus | 17 | LOCUS | T=LOCUS |
| Worksheet (1) | 18 | SPRDSHEET | T=SPRDSHEET |
| Material definition (1) | 19 | MATERIAL | T=MATERIAL |
| Polyline | 21 | POLYLINE | T=POLYLINE |
| PICT Image | 22 | PICT | T=PICT |
| Extrude | 24 | XTRD | T=XTRD |
| 3D Polygon | 25 | POLY3D | T=POLY3D |
| Layer Link | 29 | LAYERLINK | T=LAYERLINK |
| Layer | 31 |  |  |
| Sweep | 34 | SWEEP | T=SWEEP |
| Multiple extrude | 38 | MXTRD | T=MXTRD |
| Mesh | 40 | MESH | T=MESH |
| Mesh vertex | 41 |  |  |
| Record Definition (Format) | 47 |  |  |
| Record | 48 |  |  |
| Document script (1) | 49 |  |  |
| Script palette (1) | 51 |  |  |
| Worksheet Data (on drawing) | 56 |  |  |
| Dimension | 63 | DIMENSION | T=DIMENSION |
| Hatch Fill definition (1) | 66 |  |  |
| Wall | 68 | WALL | T=WALL |
| Column, Floor, Roof Face | 71 | SLAB | T=SLAB |
| Light | 81 | LIGHT | T=LIGHT |
| Roof edge | 82 |  |  |
| Roof object | 83 | ROOF | T=ROOF |
| CSG Solid (Addition, Subtraction) | 84 | CSGSOLID | T=CSGSOLID |
| Plug-in object | 86 | PLUGINOBJECT | T=PLUGINOBJECT |
| Roof element | 87 | ROOFELEMENT | T=ROOFELEMENT |
| Symbol folder (1) | 92 |  |  |
| Texture Bitmap (1) | 93 |  |  |
| Class Definition (1) | 94 |  |  |
| Solid (Cone, Sphere, ...) | 95 | SOLID | T=SOLID |
| Line Type definition (1) | 96 |  |  |
| Texture definition (1) | 97 |  |  |
| Roof Style definition (1) | 102 |  |  |
| Slab Style definition (1) | 107 |  |  |
| Tile Fill definition (1) | 108 |  |  |
| Text Style definition (1) | 109 |  |  |
| NURBS Curve | 111 | NURBSCURVE | T=NURBSCURVE |
| NURBS Surface | 113 | NURBSSURFACE | T=NURBSSURFACE |
| Renderworks Background (1) | 115 |  |  |
| Image Fill definition (1) | 119 |  |  |
| Gradient Fill definition (1) | 120 |  |  |
| Fill Space (1) | 121 |  |  |
| Viewport | 122 | VIEWPORT | T=VIEWPORT |
| Wall Style definition (1) | 127 |  |  |

**Notes:**
1. These special objects are not directly displayed in the document. They may contain definition information used by other objects or features.

## Object Subtypes

| Object | Type | Criteria Type Selector | Criteria Example |
|--------|------|------------------------|------------------|
| Directional Light | 500 | DIRLIGHT | ST=DIRLIGHT |
| Spot Light | 501 | SPOTLIGHT | ST=SPOTLIGHT |
| Point Light | 502 | POINTLIGHT | ST=POINTLIGHT |
| Custom Light | 503 | CUSTLIGHT | ST=CUSTLIGHT |
| Area Light | 504 | AREALIGHT | ST=AREALIGHT |
| Line Light | 505 | LINELIGHT | ST=LINELIGHT |
| Sheet Layer Viewport | 506 | REGVIEWPORT | ST=REGVIEWPORT |
| Section Viewport | 507 | SECTVIEWPORT | ST=SECTVIEWPORT |
| Floor | 508 | FLOOR | ST=FLOOR |
| Roof Face | 509 | ROOFFACE | ST=ROOFFACE |
| Pillar | 510 | PILLAR | ST=PILLAR |
| Cone | 511 | CONE | ST=CONE |
| Sphere | 512 | SPHERE | ST=SPHERE |
| Hemisphere | 513 | HEMISPHERE | ST=HEMISPHERE |
| Circle | 514 | CIRCLE | ST=CIRCLE |
| Opened Arc | 515 | OPENEDARC | ST=OPENEDARC |
| Solid Subtraction | 516 | CSGSUBTR | ST=CSGSUBTR |
| Solid Addition | 517 | CSGADD | ST=CSGADD |
| Solid Intersection | 518 | CSGINTER | ST=CSGINTER |
| Solid Section | 519 | CSGSECT | ST=CSGSECT |
| Solid Shell | 520 | CSGSHELL | ST=CSGSHELL |
| Chamfer | 521 | CSGCHAMFER | ST=CSGCHAMFER |
| Fillet | 522 | CSGFILLET | ST=CSGFILLET |
| Control point based NURBS surface | 523 | NURBSSURFCTRLP | ST=NURBSSURFCTRLP |
| Interpolated NURBS surface | 524 | NURBSSURFINTERP | ST=NURBSSURFINTERP |

**Notes:**
1. These special objects are not directly displayed in the document. They may contain definition information used by other objects or features.
