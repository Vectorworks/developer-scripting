# GetMarkerValue

## Description
Gets MarkerPopup value in dialog (replaces MarkerPopup procedures prior to VW2008).

```pascal
PROCEDURE GetMarkerValue(
				dialogID      : LONGINT;
				itemID        : LONGINT;
				VAR style     : INTEGER;
				VAR angle     : INTEGER;
				VAR length    : REAL;
				VAR width     : REAL;
				VAR basis     : INTEGER;
				VAR thickness : REAL);
```

```python
def vs.GetMarkerValue(dialogID, itemID):
    return (style, angle, length, width, basis, thickness)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the dialog|
|itemID|LONGINT|ID of the marker popup control|
|style|INTEGER|On return, indicates the style of the selected marker|
|angle|INTEGER|On return, indicates the angle of the selected marker (deg)|
|length|REAL|On return, indicates the length of the selected marker (inches)|
|width|REAL|On return, indicates the width of the selected marker (inches)|
|basis|INTEGER|On return, indicates the thickness basis of the selected marker.|
|thickness|REAL|On return, indicates the thickness of the selected marker.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
int, dialogID   :INTEGER;
style, angle, thicknessBasis :INTEGER;
width, length, thickness :REAL;

PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
CASE item OF
SetupDialogC:
BEGIN
style := 130;
angle := 0;
width  := .125;
length := .125;
thickness := 0;
thicknessBasis := 0;
SetMarkerValue(dialogID, 4, style, angle, width, length, thicknessBasis, thickness);
END;
5: 
BEGIN
GetMarkerValue(dialogID, 4, style, angle, width, length, thicknessBasis, thickness);

AlrtDialog(Concat(
'style: ', style, Chr(13), 
'angle: ', angle, Chr(13), 
'width: ', width,Chr(13),
'length: ', length, Chr(13),
'thickness: ', thickness, Chr(13),
'thicknessBasis: ', thicknessBasis));

END;
END;
END;

BEGIN
dialogID := CreateLayout('Test', False, 'OK', '');
CreateMarkerPopup(dialogID, 4);
CreatePushButton(dialogID, 5, '  Display Values  ');
SetFirstLayoutItem(dialogID, 4);
SetBelowItem(dialogID, 4, 5, 0, 2);
int := RunLayoutDialog(dialogID, Dialog_Handler);
END;
RUN(Example);
```
==== Python ====
```python
def Dialog_Handler( item , data ):
	if item == SetupDialogC:
		style = 130
		angle = 0
		width  = .125
		length = .125
		thickness = 0
		thicknessBasis = 0
		vs.SetMarkerValue(dialogID, 4, style, angle, width, length, thicknessBasis, thickness)
	elif item == 5: 
		style, angle, width, length, thicknessBasis, thickness = vs.GetMarkerValue(dialogID, 4)
		vs.AlrtDialog(vs.Concat(
		'style: ', style, vs.Chr(13), 
		'angle: ', angle, vs.Chr(13), 
		'width: ', width, vs.Chr(13),
		'length: ', length, vs.Chr(13),
		'thickness: ', thickness, vs.Chr(13),
		'thicknessBasis: ', thicknessBasis))



def Example():
	global SetupDialogC
	global dialogID
	SetupDialogC = 12255
	dialogID = vs.CreateLayout('Test', False, 'OK', '')
	vs.CreateMarkerPopup(dialogID, 4)
	vs.CreatePushButton(dialogID, 5, '  Display Values  ')
	vs.SetFirstLayoutItem(dialogID, 4)
	vs.SetBelowItem(dialogID, 4, 5, 0, 2)
	intt = vs.RunLayoutDialog(dialogID, Dialog_Handler)

Example()
```

## See Also
VS Functions:
[SetMarkerValue](SetMarkerValue.md)

## Version
Availability: from VectorWorks 13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
