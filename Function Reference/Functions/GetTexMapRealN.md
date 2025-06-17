# GetTexMapRealN

## Description
Get map info for specific part of object. partID is texture part, overall is 3. Selector: offsetX:1, offsetY:2, scale2D:3, rotate2D:4, radius:5, matrix mat00 through mat32: 6-17

```pascal
FUNCTION GetTexMapRealN(
				obj        : HANDLE;
				texPartID  : LONGINT;
				texLayerID : LONGINT;
				selector   : INTEGER): REAL;
```

```python
def vs.GetTexMapRealN(obj, texPartID, texLayerID, selector):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |
|texPartID|LONGINT|   |
|texLayerID|LONGINT|0 for base, &gt;0 for decals|
|selector|INTEGER|   |

## Remarks
*\_c\_* (2017.12.30): 
The radius of a part's texture on a Round Wall, fetched with the flag 5, is always mm:
<code lang="vs">
GetTexMapRealN(FSActLayer, 7, 0, 5); { radius in mm of the left part's (7) texture on a round wall }
```

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
