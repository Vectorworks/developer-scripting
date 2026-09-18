# DeleteWSRows

## Description
Deletes rows from the referenced worksheet.

```pascal
PROCEDURE DeleteWSRows(
				worksheet : HANDLE;
				startRow  : INTEGER;
				numRows   : INTEGER);
```

```python
def vs.DeleteWSRows(worksheet, startRow, numRows):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|startRow|INTEGER|Start row of delete operation.|
|numRows|INTEGER|Number of rows to be deleted.|

## Examples
```pascal
		SetLW( gPolyline, 1 );
		SetClass(gPolyLine, kPolylineClass);
		END;
		IF gCurveTable AND (gCurrentCurve < gCurveCount) THEN
			DeleteWSRows(gWorkSheetHandle, gCurrentCurve+2, gCurveCount - gCurrentCurve);
	END ELSE AlrtDialog(kInvalidSelErr);
END;

{* Delete any unused rows}
SprdSize (wksH2, nRows, nCols);
IF nRows > row + 1 THEN
	DeleteWSRows (wksH2, row + 1, nRows - row);

BEGIN
AddRows := Abs(AddRows);
DeleteWSRows(WSHand,1,AddRows);
END;
```
```python
import vs

# Deletes rows from the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
startRow = 10
numRows = 5

vs.DeleteWSRows(worksheet, startRow, numRows)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
