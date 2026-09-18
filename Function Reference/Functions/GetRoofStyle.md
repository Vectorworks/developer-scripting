# GetRoofStyle

## Description
Gets the Roof Style of a roof.

```pascal
FUNCTION GetRoofStyle(roof : HANDLE): LONGINT;
```

```python
def vs.GetRoofStyle(roof):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roof|HANDLE|The roof.|

## Examples
```pascal
resultN := GetRoofStyle(roof);
```
```python
import vs

# Gets the Roof Style of a roof.
roof = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetRoofStyle(roof)
vs.Message('GetRoofStyle returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetRoofStyle](SetRoofStyle.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
