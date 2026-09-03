# SetHeight

## Description
Set height of the passed object.

```pascal
PROCEDURE SetHeight(
				h     : HANDLE;
				value : REAL);
```

```python
def vs.SetHeight(h, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|value|REAL|The new height of the object.|

## Examples
```pascal
SetHeight(h, 1.0);
```
```python
import vs

# Set height of the passed object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
value = 1.0

vs.SetHeight(h, value)
```

## Version
Availability: from Vectorworks14.0

## Category
* [Object Info](../Categories/Object%20Info.md)
