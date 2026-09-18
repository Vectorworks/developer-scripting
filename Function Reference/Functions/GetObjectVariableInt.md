# GetObjectVariableInt

## Description
Returns the value of a VectorWorks object property. Used with properties returning an INTEGER value.

For specific object selector index values, see the [Script Appendix](../Appendix/pages/Appendix%20G%20-%20Object%20Selectors.md).

```pascal
FUNCTION GetObjectVariableInt(
				h     : HANDLE;
				index : INTEGER): INTEGER;
```

```python
def vs.GetObjectVariableInt(h, index):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|

## Examples
[ComplexDialogLayout4](examples/ComplexDialogLayout4.md)

```pascal
ok := FALSE;
if ( GetType(h) = 68 ) then BEGIN
	h1 := WallFootPrint(h);
	ok := TRUE;
END else if (GetType(h) = 71) & (GetObjectVariableInt(h, 172) = 3) then BEGIN
	h1 := HDuplicate(FIn3D(h), 0, 0);
	ok := TRUE;
END;

BEGIN
		DefaultWSFontID := GetObjectVariableInt(tempHandle,86);
		SetWSPlacement(tempHandle,130,223,698,816);
		{SetObjectVariableInt(tempHandle,86,0);} {Don't do this!!!!}
		SetObjectVariableInt(tempHandle,87,10);
		{Column Widths}

{Check to see if there is already a seating layout WS in the document
IF NOT THEN create one.}
IF GetObject(kSeatingCount) = NIL THEN BEGIN
	MyWSHandle := CreateWS(kSeatingCount, 3, 5);
	DefaultWSFontID := GetObjectVariableInt(MyWSHandle,86);
	ShowWS(MyWSHandle, FALSE); {Hide the WS while we create it}
	SetWSColumnWidth   (MyWSHandle, 1, 1, (19 * 12));
	SetWSColumnWidth   (MyWSHandle, 2, 2, (8 * 12));
	SetWSCellTextFormat(MyWSHandle, 1, 1, 1, 5, DefaultWSFontID, 14, 1);
```
```python
if vs.GetObjectVariableInt( containerHandle, 154 ) == 2:
	containerType = -containerType #{sheet layer}
```
See also in tutorials: [29. Cross-Layer Summary](ai%20examples/29_WorksheetCrossLayerSummary.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
