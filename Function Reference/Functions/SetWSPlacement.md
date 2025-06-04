# SetWSPlacement

## Description
Sets the on-screen location and dimensions of the referenced worksheets' window.

```pascal
PROCEDURE SetWSPlacement(
				worksheet : HANDLE;
				top       : INTEGER;
				left      : INTEGER;
				bottom    : INTEGER;
				right     : INTEGER);
```

```python
def vs.SetWSPlacement(worksheet, top, left, bottom, right):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|top|INTEGER|X-coordinate of top left corner of worksheet window.|
|left|INTEGER|Y-coordinate of top left corner of worksheet window.|
|bottom|INTEGER|X-coordinate of bottom right corner of worksheet window.|
|right|INTEGER|Y-coordinate of bottom right corner of worksheet window.|

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
