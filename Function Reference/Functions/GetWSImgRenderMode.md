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

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
