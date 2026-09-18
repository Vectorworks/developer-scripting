# GetWSImgAngle

## Description
Gets the specified worksheet cell's image angle.

```pascal
PROCEDURE GetWSImgAngle(
				worksheet    : HANDLE;
				row          : INTEGER;
				column       : INTEGER;
				VAR NewParam : REAL);
```

```python
def vs.GetWSImgAngle(worksheet, row, column):
    return NewParam
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|   |
|row|INTEGER|The cell row.|
|column|INTEGER|The cell column.|
|NewParam|REAL|The image angle.|

## Examples
```pascal
GetWSImgAngle(worksheet, 1, 2, 1.0);
```
```python
import vs

# Gets the specified worksheet cell's image angle.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

result = vs.GetWSImgAngle(worksheet, row, column)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
