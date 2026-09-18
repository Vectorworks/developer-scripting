# TargetSprdSheet

## Description
Procedure TargetSprdSheet selects the referenced worksheet as the active worksheet for the document. The worksheet is not opened onscreen.

```pascal
PROCEDURE TargetSprdSheet(h : HANDLE);
```

```python
def vs.TargetSprdSheet(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to worksheet.|

## Remarks
This selects a spreadsheet for use by the script.  It does not open the spreadsheet. [sd 8/18/98]

## Examples
```pascal
TargetSprdSheet (wksH2);
SetWSCellFormula (wksH2, 1, 2, 1, 2, Num2Str (2, gIndex_Data));
IF (followerType = 3) OR (followerType = 4) THEN
BEGIN
	SetWSCellFormula (wksH2, r0, 5, r0, 5, GetPlugInString (6026));

BEGIN
	wksH := CreateWS (GetPlugInString (10001), kStartRow2 + kNumLoads + 1, 7);
	TargetSprdSheet (wksH);
	TextSize (kWSTextSize);
	SetWSColumnWidth (wksH, 1, 1, 165);
	SetWSColumnWidth (wksH, 2, 7, 120);

{* Clear the load data from the worksheet *}
TargetSprdSheet (wksH);
TextSize (kWSTextSize);
FOR i := 1 TO kMaxLoads DO
BEGIN
	FOR j := 1 TO kNumCols DO
```
```python
import vs

# Procedure TargetSprdSheet selects the referenced worksheet as the active
# worksheet for the document.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.TargetSprdSheet(h)
```

## See Also
[SetTopVisibleWS](SetTopVisibleWS.md)

## Version
TargetSprdSheet is obsolete as of VectorWorks 9.0, see new [ SetTopVisibleWS](SetTopVisibleWS.md).

Availability: from VectorWorks 8.0

## Category
* [Worksheets](../Categories/Worksheets.md)
