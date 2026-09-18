# TrueTypeToPoly

## Description
TrueTypeToPoly converts handle to Text object into handle to Group of poly objects with similar shape.

```pascal
FUNCTION TrueTypeToPoly(
				textHandle          : HANDLE;
				VAR polyGroupHandle : HANDLE): LONGINT;
```

```python
def vs.TrueTypeToPoly(textHandle):
    return (LONGINT, polyGroupHandle)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textHandle|HANDLE|   |
|polyGroupHandle|HANDLE|   |

## Examples
```pascal
result := TrueTypeToPoly(textHandle, groupHandle);
HScale2D(groupHandle, 0, 0, 1 / layerScale, 1 / layerScale, TRUE);
```
```python
import vs

# TrueTypeToPoly converts handle to Text object into handle to Group of poly
# objects with similar shape.
textHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN, polyGroupHandle = vs.TrueTypeToPoly(textHandle)
vs.Message('TrueTypeToPoly returned: ' + str((resultN, polyGroupHandle)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
