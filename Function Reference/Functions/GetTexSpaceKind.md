# GetTexSpaceKind

## Description
Function GetTexSpaceKind returns the object type for texture mapping space.

{| class="wikitable_c"
|+ Table - Texture Mapping Spaces
! Date Style !! Constant
|-
| Plane
| style="text-align:center"| 0
|-
| Sphere
| style="text-align:center"| 1
|-
| Cylinder
| style="text-align:center"| 2
|-
| Algorithmic
| style="text-align:center"| 3
|}

```pascal
FUNCTION GetTexSpaceKind(textureSpace : HANDLE): INTEGER;
```

```python
def vs.GetTexSpaceKind(textureSpace):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|

## Remarks
[[User:CBM-c-|_c_]], (2018.12.29) Use [[VS:GetTexMapIntN]] instead. 


Returns the kind of the texture mapping space; 0 = Plane space, 1 = Sphere, 2 = Cylinder, and 3 = Algorithmic (Perimeter or Roof)

Note: GetTexMapXXX routines replace the older GetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks 8.0

## Category
* Textures

