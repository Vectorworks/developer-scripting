# ShowWS

## Description
Sets the display status of the referenced worksheet.

```pascal
PROCEDURE ShowWS(
				worksheet : HANDLE;
				show      : BOOLEAN);
```

```python
def vs.ShowWS(worksheet, show):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|show|BOOLEAN|Desired display status of worksheet|

## Examples
```pascal
BEGIN
RecalculateWS(GetObject(kRLwkshtName));
ResetObject(GetObject(kRLwkshtName));
ShowWS(GetObject(kRLwkshtName),TRUE);
WSImage := GetWSImage(GetObject(kRLwkshtName));
IF WSImage <> NIL THEN ResetObject(WSImage);
END

IF NOT THEN create one.}
IF GetObject(kSeatingCount) = NIL THEN BEGIN
	MyWSHandle := CreateWS(kSeatingCount, 3, 5);
	DefaultWSFontID := GetObjectVariableInt(MyWSHandle,86);
	ShowWS(MyWSHandle, FALSE); {Hide the WS while we create it}
	SetWSColumnWidth   (MyWSHandle, 1, 1, (19 * 12));
	SetWSColumnWidth   (MyWSHandle, 2, 2, (8 * 12));
	SetWSCellTextFormat(MyWSHandle, 1, 1, 1, 5, DefaultWSFontID, 14, 1);

BEGIN
	CASE gFindMode OF
	1:	BEGIN
			ShowWS( WSh, TRUE );
			SetTopVisibleWS( WSh );
			SetWSCurrentCell(WSh, row, col);
			ProcessFoundCell := TRUE;
		END;
```
```python
import vs

# Sets the display status of the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
show = True

vs.ShowWS(worksheet, show)
```
See also in tutorials: [21. Hello Worksheet — Create and Populate](ai%20examples/21_WorksheetBasic.md), [22. Selected Objects → Worksheet Rows](ai%20examples/22_WorksheetSelectedObjects.md), [23. Count Objects by Criteria (Formula-Driven)](ai%20examples/23_WorksheetCountByCriteria.md), [24. Auto-Populating Database Row](ai%20examples/24_WorksheetDBRowAutoPopulate.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
