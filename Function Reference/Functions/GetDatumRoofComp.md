# GetDatumRoofComp

## Description
Gets the datum roof component of the object.

```pascal
FUNCTION GetDatumRoofComp(object : HANDLE): INTEGER;
```

```python
def vs.GetDatumRoofComp(object):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|

## Examples
```pascal
resultN := GetDatumRoofComp(object);
```
```python
import vs

# Gets the datum roof component of the object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetDatumRoofComp(object)
vs.Message('GetDatumRoofComp returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetDatumRoofComp](SetDatumRoofComp.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
