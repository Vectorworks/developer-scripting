# SetTexSpaceKind

## Description
Procedure SetTexSpaceKind sets the object type for referenced texture mapping space.

* Table - Texture Mapping Spaces

| Date Style | Constant |
|------------|----------|
| Plane | 0 |
| Sphere | 1 |
| Cylinder | 2 |
| Algorithmic | 3 |


```pascal
PROCEDURE SetTexSpaceKind(
				textureSpace : HANDLE;
				kind         : INTEGER);
```

```python
def vs.SetTexSpaceKind(textureSpace, kind):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|kind|INTEGER|Texture mapping space type.|

## Remarks
Sets the kind for the texture mapping space; 0 = Plane space, 1 = Sphere, 2 = Cylinder, and 3 = Algorithmic (Perimeter or Roof)

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks 8.0

## Category
* [Textures](../Categories/Textures.md)
