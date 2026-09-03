# GetWSImgRenderMode

## Description
Gets the specified worksheet cell's image render mode

```pascal
PROCEDURE GetWSImgRenderMode(
				worksheet      : HANDLE;
				row            : INTEGER;
				column         : INTEGER;
				VAR renderMode : INTEGER);
```

```python
def vs.GetWSImgRenderMode(worksheet, row, column):
    return renderMode
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|The worksheet handle.|
|row|INTEGER|The cell row.|
|column|INTEGER|The cell column.|
|renderMode|INTEGER|The image render mode.|

## Remarks
Wire Frame render mode  = 0,<BR>
Hidden Line render mode = 6,<BR>
OpenGL render mode       = 11.

## Examples
```pascal
GetWSImgRenderMode(worksheet, 1, 2, 3);
```
```python
import vs

# Gets the specified worksheet cell's image render mode.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

result = vs.GetWSImgRenderMode(worksheet, row, column)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
