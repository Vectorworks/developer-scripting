# GetNumTexLayers

## Description
Returns number of texture layers (base + decals) for the specified part.

```pascal
FUNCTION GetNumTexLayers(
				obj       : HANDLE;
				texPartID : LONGINT): LONGINT;
```

```python
def vs.GetNumTexLayers(obj, texPartID):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |
|texPartID|LONGINT|   |

## Remarks
*_c_*, (2017.12.29) For the texPartID flags, check the SDK file RenderOptionsValues.h:
: 3: overall for any kind of object
: 4: top in extrudes/sweeps
: 5: bottom in extrudes/sweeps
: 6: sides in extrudes/sweeps
: 7: left in walls
: 8: right in walls
: 9: start cap in walls
: 10: end cap in walls
: 11: top in walls
: 12: bottom in walls
: 13: holes in walls
: 14: top in roof faces/slabs 
: 15: bottom in roof faces/slabs 
: 16: sides in roof faces/slabs 
: 17: top in roofs 
: 18: bottom in roofs 
: 19: sides in roofs
: 20: gable in roofs
: 21: fascia in roofs
: 22: attic in roofs
: 23: soffit in roofs
: 24: dutch walls in roofs
: 25: dormer walls in roofs
: 26: frame cap in curtain walls
: 27: panel face in curtain walls

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
