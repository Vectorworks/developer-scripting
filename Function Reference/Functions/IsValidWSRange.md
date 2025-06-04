# IsValidWSRange

## Description
Returns whether the specified range is within the valid range of the referenced worksheet.

```pascal
FUNCTION IsValidWSRange(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER): BOOLEAN;
```

```python
def vs.IsValidWSRange(worksheet, topRow, leftColumn, bottomRow, rightColumn):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|topRow|INTEGER|Top row of target range.|
|leftColumn|INTEGER|Leftmost column of target range.|
|bottomRow|INTEGER|Bottom row of target range.|
|rightColumn|INTEGER|Rightmost column of target range.|

## Remarks
Determines if specified range is valid for the specified worksheet.
NOTE: A determination that a range is valid only means that the specified range falls within a range of 0 to the current number of worksheet rows and 0 to the current number of worksheet columns. A valid range does not imply that every worksheet SDK function will accept that range. The user should always  note any specific cell and cell range restrictions of a call they may use.

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
