# CreateEditReal

## Description
Creates an editable text field control for REAL values.

CreateEditReal is intended specifically for entry of numeric values; the control returns values in a numeric format, and supports calculations within the control field.

{| class="wikitable_c"
|+ Table - Field Types for EditReal Fields
! Index !! Field Value
|-
| 1
| REAL value
|-
| 2
| Angular value
|-
| 3
| Dimension
|-
| 4
| X coordinate
|-
| 5
| Y coordinate
|}

```pascal
PROCEDURE CreateEditReal(
				dialogID          : LONGINT;
				itemID            : LONGINT;
				editRealType      : LONGINT;
				defaultValue      : REAL;
				widthInCharacters : LONGINT);
```

```python
def vs.CreateEditReal(dialogID, itemID, editRealType, defaultValue, widthInCharacters):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|editRealType|LONGINT|The type of REAL value being accepted.|
|defaultValue|REAL|Default value for the field.|
|widthInCharacters|LONGINT|Width of the field in characters.|

## Remarks
Edits reals, does math,  get and set values with get and set real calls.

There are 5 edit real types:
*1 - Real, regular old real type;
*2 - Angle, vs input and output is always in degrees but the user can use what ever they want;
*3 - Dimension, usually an offset this a distance that is not tied to the origin;
*4 - CoordinateX, this is an exact x location on the drawing;
*5 - CoordinateY, this is an exact y location on the drawing. There are separate x and y controls to account for changes the user may make to the origin. I think Z coordinates should use the offset mode, but I need to check with mark on this one.

The default value parameter isn't worth much -- it plops the value into the edit box OK -- but it does not assign the value to the control. [[VS:GetEditReal]] will return 0 for the control, unless the user clicks in the control. Use SetEditReal in your SetupDialogC event instead of using a default value for this control.

Accepts '3 1/4' and '3000000' but not '3,000,000'.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
dialog1 :INTEGER;
result  :INTEGER;
PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
END;
BEGIN
dialog1 := CreateLayout('Example Dialog', FALSE, 'OK', 'Cancel');
CreateEditReal(dialog1, 4, 3, 123, 16);
SetFirstLayoutItem(dialog1, 4);
result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```
==== Python ====
```python
def Dialog_Handler( item , data ):
	pass
def Example():
	dialog1 = vs.CreateLayout('Example Dialog', False, 'OK', 'Cancel')
	vs.CreateEditReal(dialog1, 4, 3, 123, 16)
	vs.SetFirstLayoutItem(dialog1, 4)
	result = vs.RunLayoutDialog(dialog1, Dialog_Handler)
Example()
```

## Version
Availability: from VectorWorks 9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
