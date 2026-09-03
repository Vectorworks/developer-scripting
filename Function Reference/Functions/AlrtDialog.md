# AlrtDialog

## Description
Procedure AlrtDialog displays an alert dialog to the user.

```pascal
PROCEDURE AlrtDialog(message : STRING);
```

```python
def vs.AlrtDialog(message):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|STRING|The alert message to be displayed.|

## Remarks
If message is null, the dialog will not be displayed.

## Examples
#### VectorScript ####
```pascal
AlrtDialog('No objects are selected for this operation.');
```
#### Python ####
```python
vs.AlrtDialog('No objects are selected for this operation.')
```

```pascal
IF NOT IntersLineLine(p1, p2, p3, p4, theCenter) THEN AlrtDialog(GetPlugInString(3001))
ELSE
BEGIN
	theArea := TriArea(p2[1], p2[2], p3[1], p3[2], theCenter[1], theCenter[2]);
	IF (theArea > 0) THEN
		sign := 1
	ELSE sign := -1;

BEGIN
	SysBeep;
	AlrtDialog (alertMsg1);
	item := -1;
END;

BEGIN
	Sysbeep;
	AlrtDialog (GetPlugInString (3018));
	SetItemText(dialogID, 6, '1');
	SelectEditText(dialogID, 6);
	item := -1;
END;
```
```python
if str == '':
	str = ' '
vs.AlrtDialog( str )
```
See also in tutorials: [06. Boolean Solids: Drill a Hole Through a Block](ai%20examples/06_BooleanSolids.md), [22. Selected Objects → Worksheet Rows](ai%20examples/22_WorksheetSelectedObjects.md), [25. Geometric Property Extraction Table](ai%20examples/25_WorksheetPolyGeometry.md), [27. Formatted Wall Schedule](ai%20examples/27_WorksheetFormattedSchedule.md)

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
