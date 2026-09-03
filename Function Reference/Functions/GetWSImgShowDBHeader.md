# GetWSImgShowDBHeader

## Description
Check whether worksheet image is set to show database headers.

```pascal
FUNCTION GetWSImgShowDBHeader(hWorksheetImage : HANDLE): BOOLEAN;
```

```python
def vs.GetWSImgShowDBHeader(hWorksheetImage):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hWorksheetImage|HANDLE|   |

## Examples
```pascal
resultOK := GetWSImgShowDBHeader(hWorksheetImage);
```
```python
import vs

# Check whether worksheet image is set to show database headers.
hWorksheetImage = vs.GetObject('MyWorksheet')  # handle to a worksheet

ok = vs.GetWSImgShowDBHeader(hWorksheetImage)
if ok:
    vs.Message('GetWSImgShowDBHeader succeeded')
else:
    vs.Message('GetWSImgShowDBHeader failed')
```

## Version
Availability: from Vectorworks 2018

## Category
* [Worksheets](../Categories/Worksheets.md)
