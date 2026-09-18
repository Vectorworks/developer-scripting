# GetTexMapInt

## Description
Get map info for specific part of object. partID is texture part, overall is 3. Selector should be1, to return the texture map type integer.

```pascal
FUNCTION GetTexMapInt(
				h        : HANDLE;
				partID   : LONGINT;
				selector : INTEGER): INTEGER;
```

```python
def vs.GetTexMapInt(h, partID, selector):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|partID|LONGINT|   |
|selector|INTEGER|   |

## Examples
```pascal
resultN := GetTexMapInt(h, 1, 2);
```
```python
import vs

# Get map info for specific part of object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
partID = 1
selector = 2

resultN = vs.GetTexMapInt(h, partID, selector)
vs.Message('GetTexMapInt returned: ' + str(resultN))
```

## See Also
[GetTexMapIntN](GetTexMapIntN.md), [SetTexMapIntN](SetTexMapIntN.md)

## Version
Availability: from Vectorworks 14.0. Deprecated from Vectorworks 15.0.

## Category
* [Textures](../Categories/Textures.md)
