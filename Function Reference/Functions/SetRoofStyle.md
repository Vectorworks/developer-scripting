# SetRoofStyle

## Description
Sets the Roof Style of a roof.

```pascal
PROCEDURE SetRoofStyle(
				roof      : HANDLE;
				roofStyle : LONGINT);
```

```python
def vs.SetRoofStyle(roof, roofStyle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roof|HANDLE|The roof.|
|roofStyle|LONGINT|The Roof Style.|

## Examples
```pascal
SetRoofStyle(roof, 1);
```
```python
import vs

# Sets the Roof Style of a roof.
roof = vs.FSActLayer()  # handle to the first selected object on the active layer
roofStyle = 0

vs.SetRoofStyle(roof, roofStyle)
```

## See Also
VS Functions:
[GetRoofStyle](GetRoofStyle.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
