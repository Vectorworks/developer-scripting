# PtDialog

## Description
Procedure PtDialog displays a dialog box which requests the user to enter a coordinate (point) value.

```pascal
PROCEDURE PtDialog(
				request  : STRING;
				defaultX : STRING;
				defaultY : STRING;
				VAR x    : REAL;
				VAR y    : REAL);
```

```python
def vs.PtDialog(request, defaultX, defaultY):
    return (x, y)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|request|STRING|Dialog user prompt string.|
|defaultX|STRING|Default value for input field.|
|defaultY|STRING|Default value for input field.|
|x|REAL|Returns user input X value.|
|y|REAL|Returns user input Y value.|

## Examples
#### VectorScript ####
```pascal
PtDialog('Enter a coordinate.','0','0',cX,cY);
```
#### Python ####
```python

```

```pascal
BEGIN
	TxtX := GetRField(Obj,kHoistPIOName,'ControlPoint01X');
	TxtY := GetRField(Obj,kHoistPIOName,'ControlPoint01Y');
	PtDialog(CONCAT('Input location measured from the insertion of the hoist.',chr(13),'the hoist graphic center'),TxtX,TxtY,X,Y);
	IF (NOT DidCancel) THEN
		ForEachObject(AssignTextPosition, (((R IN [kHoistPIOName]) & (SEL=TRUE))));
END
```
```python
result = vs.PtDialog(request, defaultX, defaultY)
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
