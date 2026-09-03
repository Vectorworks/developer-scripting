# AreWorksheetGridLinesVisible

## Description
Determines the status of the grid lines visibility for the specified worksheet.

```pascal
FUNCTION AreWorksheetGridLinesVisible(h : HANDLE): BOOLEAN;
```

```python
def vs.AreWorksheetGridLinesVisible(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to worksheet.|

## Examples
```pascal
resultOK := AreWorksheetGridLinesVisible(h);
```
```python
import vs

# Determines the status of the grid lines visibility for the specified worksheet.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.AreWorksheetGridLinesVisible(h)
if ok:
    vs.Message('AreWorksheetGridLinesVisible succeeded')
else:
    vs.Message('AreWorksheetGridLinesVisible failed')
```

## Version
Availability: from Vectorworks 2011

## Category
* [Worksheets](../Categories/Worksheets.md)
