# GetTexMapBool

## Description
Get map info for specific part of object. partID is texture part, overall is 3.

Selector:
*init: 1
*flip: 2
*repH: 3
*repV: 4
*long edge: 5
*worldZ: 6
*auto align: 7

```pascal
FUNCTION GetTexMapBool(
				h        : HANDLE;
				partID   : LONGINT;
				selector : INTEGER): BOOLEAN;
```

```python
def vs.GetTexMapBool(h, partID, selector):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|partID|LONGINT|   |
|selector|INTEGER|   |

## Examples
```pascal
resultOK := GetTexMapBool(h, 1, 2);
```
```python
import vs

# Get map info for specific part of object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
partID = 1
selector = 2

ok = vs.GetTexMapBool(h, partID, selector)
if ok:
    vs.Message('GetTexMapBool succeeded')
else:
    vs.Message('GetTexMapBool failed')
```

## See Also
VS Functions:
* VW 14: [SetTexMapBool](SetTexMapBool.md)
* from VW 15: [SetTexMapBoolN](SetTexMapBoolN.md)
* from VW 15: [GetTexMapBoolN](GetTexMapBoolN.md)

## Version
Availability: from Vectorworks 14.0. Deprecated from Vectorworks 15.0.

## Category
* [Textures](../Categories/Textures.md)
