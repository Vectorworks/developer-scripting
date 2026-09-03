# CountFillSpaces

## Description
Returns the number of fill spaces currently attached to a specified object.

```pascal
FUNCTION CountFillSpaces(h : HANDLE): INTEGER;
```

```python
def vs.CountFillSpaces(h):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the object containing the fill spaces to be counted.|

## Examples
```pascal
resultN := CountFillSpaces(h);
```
```python
import vs

# Returns the number of fill spaces currently attached to a specified object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.CountFillSpaces(h)
vs.Message('CountFillSpaces returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
