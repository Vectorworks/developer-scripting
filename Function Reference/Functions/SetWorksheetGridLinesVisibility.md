# SetWorksheetGridLinesVisibility

## Description
Sets the visibility of the grid lines for the specified worksheet.

```pascal
PROCEDURE SetWorksheetGridLinesVisibility(
				h       : HANDLE;
				visible : BOOLEAN);
```

```python
def vs.SetWorksheetGridLinesVisibility(h, visible):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to worksheet.|
|visible|BOOLEAN|The grid line visibility flag.|

## Examples
```pascal
SetWorksheetGridLinesVisibility(h, TRUE);
```
```python
import vs

# Sets the visibility of the grid lines for the specified worksheet.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
visible = True

vs.SetWorksheetGridLinesVisibility(h, visible)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Worksheets](../Categories/Worksheets.md)
