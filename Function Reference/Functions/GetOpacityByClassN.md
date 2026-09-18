# GetOpacityByClassN

```pascal
PROCEDURE GetOpacityByClassN(
				h                        : HANDLE;
				VAR isPenOpacityByClass  : BOOLEAN;
				VAR isFillOpacityByClass : BOOLEAN);
```

```python
def vs.GetOpacityByClassN(h):
    return (isPenOpacityByClass, isFillOpacityByClass)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|isPenOpacityByClass|BOOLEAN|   |
|isFillOpacityByClass|BOOLEAN|   |

## Examples
```pascal
GetOpacityByClassN(h, TRUE, FALSE);
```
```python
import vs

h = vs.FSActLayer()  # handle to the first selected object on the active layer

isPenOpacityByClass, isFillOpacityByClass = vs.GetOpacityByClassN(h)
vs.Message('GetOpacityByClassN returned: ' + str((isPenOpacityByClass, isFillOpacityByClass)))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
