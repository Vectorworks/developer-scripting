# SetObjectVariableHandle

## Description
Sets the value of a VectorWorks object property.

```pascal
PROCEDURE SetObjectVariableHandle(
				h     : HANDLE;
				index : INTEGER;
				value : HANDLE);
```

```python
def vs.SetObjectVariableHandle(h, index, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|index|INTEGER|   |
|value|HANDLE|   |

## Examples
```pascal
BEGIN
SetObjectVariableHandle(vpHandle, 1046, pluginH);
ReDrawAll;
END;

IF drawingInVP THEN BEGIN
	{This call will move the newly created dimension to where it should be in the viewport annotation layer.}
	SetObjectVariableHandle(LNewObj, 1234, containerHandle);
END;
```
```python
import vs

# Sets the value of a VectorWorks object property.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1
value = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

vs.SetObjectVariableHandle(h, index, value)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Object Info](../Categories/Object%20Info.md)
