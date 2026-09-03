# CreateWS

## Description
Creates a new worksheet in a VectorWorks document.

```pascal
FUNCTION CreateWS(
				name    : STRING;
				rows    : INTEGER;
				columns : INTEGER): HANDLE;
```

```python
def vs.CreateWS(name, rows, columns):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|The name of the worksheet.|
|rows|INTEGER|The number of rows in the worksheet.|
|columns|INTEGER|The number of columns in the worksheet.|

## Remarks
Creates a new worksheet object with the specified name and number of rows and columns.
If the name is in use, a legal available name based on the specified name will be used instead.
The number of rows must be >= 1 and <= 4094.
The number of columns must be >= 1 and <= 256.
NOTE: To create an on-drawing worksheet object, pass a worksheet handle to [CreateWSImage](CreateWSImage.md).

## Examples
```pascal
BEGIN
{Creation/Placement}
tempHandle := CreateWS(kRLwkshtName,11,3);
IF tempHandle <> NIL THEN
BEGIN
		DefaultWSFontID := GetObjectVariableInt(tempHandle,86);
		SetWSPlacement(tempHandle,130,223,698,816);

{Check to see if there is already a seating layout WS in the document
IF NOT THEN create one.}
IF GetObject(kSeatingCount) = NIL THEN BEGIN
	MyWSHandle := CreateWS(kSeatingCount, 3, 5);
	DefaultWSFontID := GetObjectVariableInt(MyWSHandle,86);
	ShowWS(MyWSHandle, FALSE); {Hide the WS while we create it}
	SetWSColumnWidth   (MyWSHandle, 1, 1, (19 * 12));
	SetWSColumnWidth   (MyWSHandle, 2, 2, (8 * 12));

		wsHand := NIL;
	END;
END;
if wsHand = nil then BEGIN
	wsHand := CreateWS(wsName, kNumRows, kNumCols);
	SetWSPlacement          (wsHand, 186, 49, 450, 672);
	SetObjectVariableString (wsHand, 80, wsName); {Worksheet Header}
	SetObjectVariableBoolean(wsHand, 82, FALSE);  {Show Database Header}
	SetObjectVariableBoolean(wsHand, 83, FALSE);  {Show Gridlines}
```
```python
import vs

# Creates a new worksheet in a VectorWorks document.
name = 'Example'
rows = 10
columns = 5

wsHandle = vs.CreateWS(name, rows, columns)
if wsHandle is not None:
    vs.Message('Created object handle: ' + str(wsHandle))
```
See also in tutorials: [21. Hello Worksheet — Create and Populate](ai%20examples/21_WorksheetBasic.md), [22. Selected Objects → Worksheet Rows](ai%20examples/22_WorksheetSelectedObjects.md), [23. Count Objects by Criteria (Formula-Driven)](ai%20examples/23_WorksheetCountByCriteria.md), [24. Auto-Populating Database Row](ai%20examples/24_WorksheetDBRowAutoPopulate.md)

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
