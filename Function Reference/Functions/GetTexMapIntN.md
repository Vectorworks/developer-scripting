# GetTexMapIntN

## Description
Get map info for specific part of object. partID is texture part, overall is 3. Selector should be 1, to return the texture map type integer.

```pascal
FUNCTION GetTexMapIntN(
				obj        : HANDLE;
				texPartID  : LONGINT;
				texLayerID : LONGINT;
				selector   : INTEGER): INTEGER;
```

```python
def vs.GetTexMapIntN(obj, texPartID, texLayerID, selector):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |
|texPartID|LONGINT|   |
|texLayerID|LONGINT|0 for base, &gt;0 for decals|
|selector|INTEGER|   |

## Remarks
(*_c_*, 2017 Dec. 29) 
Texture Mapping Types:
* Plane		0
* Sphere	1
* Cylinder	2
* Perimeter	3

If it's set on Auto-align GetTexMapIntN returns the appropriate flag depending on the object

## Examples
```python
{ _c_: returns the mapping type (plane, sphere, cylinder, perimeter) of the overall texture }
GetTexMapIntN(obj, 3, 0, 1);
```

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
