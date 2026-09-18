# IsWSVisible

## Description
Returns display status of referenced worksheet.

```pascal
FUNCTION IsWSVisible(worksheet : HANDLE): BOOLEAN;
```

```python
def vs.IsWSVisible(worksheet):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|

## Examples
```pascal
resultOK := IsWSVisible(worksheet);
```
```python
import vs

# Returns display status of referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet

ok = vs.IsWSVisible(worksheet)
if ok:
    vs.Message('IsWSVisible succeeded')
else:
    vs.Message('IsWSVisible failed')
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
