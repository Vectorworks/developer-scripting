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
|texLayerID|LONGINT|0 for base, >0 for decals|
|selector|INTEGER|   |

## Remarks
*\_c\_* (2017.12.30): 
The radius of a part's texture on a Round Wall, fetched with the flag 5, is always mm:
```pascal
GetTexMapRealN(FSActLayer, 7, 0, 5); { radius in mm of the left part's (7) texture on a round wall }
```

## Examples
```pascal
resultVal := GetTexMapRealN(obj, 1, 2, 3);
```
```python
import vs

# Get map info for specific part of object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
texPartID = 1
texLayerID = 2
selector = 3

value = vs.GetTexMapRealN(obj, texPartID, texLayerID, selector)
vs.Message('GetTexMapRealN returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
