# GetWSImgType

## Description
Gets the specified worksheet cell's image type.

```pascal
PROCEDURE GetWSImgType(
				worksheet : HANDLE;
				row       : INTEGER;
				column    : INTEGER;
				VAR type  : INTEGER);
```

```python
def vs.GetWSImgType(worksheet, row, column):
    return type
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|The worksheet handle.|
|row|INTEGER|The cell row.|
|column|INTEGER|The cell column.|
|type|INTEGER|The image type.|

## Remarks
Thumbnail image type     = 0,<BR>
2D Attributes image type = 1.

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
