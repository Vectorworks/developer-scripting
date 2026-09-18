# GetWSImageScaleF

## Description
Returns the scale factor of the specified worksheet on drawing object.

```pascal
FUNCTION GetWSImageScaleF(handle : HANDLE): REAL;
```

```python
def vs.GetWSImageScaleF(handle):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|The handle to the worksheet on drawing object.|

## Examples
```pascal
resultVal := GetWSImageScaleF(handle);
```
```python
import vs

# Returns the scale factor of the specified worksheet on drawing object.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.GetWSImageScaleF(handle)
vs.Message('GetWSImageScaleF returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Worksheets](../Categories/Worksheets.md)
