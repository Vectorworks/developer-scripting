# SetWidth

## Description
Set width of the passed object.

```pascal
PROCEDURE SetWidth(
				h     : HANDLE;
				value : REAL);
```

```python
def vs.SetWidth(h, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|value|REAL|The new width of the object.|

## Examples
```pascal
SetWidth(h, 1.0);
```
```python
import vs

# Set width of the passed object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
value = 1.0

vs.SetWidth(h, value)
```

## Version
Availability: from Vectorworks14.0

## Category
* [Object Info](../Categories/Object%20Info.md)
