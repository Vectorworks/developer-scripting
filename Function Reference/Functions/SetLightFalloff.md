# SetLightFalloff

## Description
Procedure SetLightFalloff sets the fall off attributes for the referenced light object.

{| class="wikitable_c"
|+ Table - Light Falloff Types
! Falloff Type !! Constant
|-
| None
| 0
|-
| Normal
| 1
|-
| Smooth
| 2
|-
| Sharp
| 3
|}

```pascal
PROCEDURE SetLightFalloff(
				light       : HANDLE;
				distFalloff : INTEGER;
				angFalloff  : INTEGER);
```

```python
def vs.SetLightFalloff(light, distFalloff, angFalloff):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|light|HANDLE|Handle to light.|
|distFalloff|INTEGER|Distance falloff value.|
|angFalloff|INTEGER|Angular falloff value.|

## Remarks
Sets the falloff functions for the light.  0 = None, 1 = Normal, 2 = Smooth, 3 = Sharp (angular falloff only).

## Version
Availability: from MiniCAD 7.0.1

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
