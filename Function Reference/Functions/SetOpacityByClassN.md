# SetOpacityByClassN

```pascal
PROCEDURE SetOpacityByClassN(
				h                      : HANDLE;
				inIsPenOpacityByClass  : BOOLEAN;
				inIsFillOpacityByClass : BOOLEAN);
```

```python
def vs.SetOpacityByClassN(h, inIsPenOpacityByClass, inIsFillOpacityByClass):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|inIsPenOpacityByClass|BOOLEAN|   |
|inIsFillOpacityByClass|BOOLEAN|   |

## Examples
```pascal
SetOpacityByClassN(h, TRUE, FALSE);
```
```python
import vs

h = vs.FSActLayer()  # handle to the first selected object on the active layer
inIsPenOpacityByClass = True
inIsFillOpacityByClass = True

vs.SetOpacityByClassN(h, inIsPenOpacityByClass, inIsFillOpacityByClass)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
