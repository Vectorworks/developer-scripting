# GetWSPlacement

## Description
Returns the on-screen location of the referenced worksheets' window.

```pascal
PROCEDURE GetWSPlacement(
				worksheet  : HANDLE;
				VAR top    : INTEGER;
				VAR left   : INTEGER;
				VAR bottom : INTEGER;
				VAR right  : INTEGER);
```

```python
def vs.GetWSPlacement(worksheet):
    return (top, left, bottom, right)
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
