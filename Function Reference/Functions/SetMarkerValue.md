# SetMarkerValue

## Description
Sets MarkerPopup value in dialog (replaces MarkerPopup procedures prior to VW2008).

```pascal
PROCEDURE SetMarkerValue(
				dialogID  : LONGINT;
				itemID    : LONGINT;
				style     : INTEGER;
				angle     : INTEGER;
				length    : REAL;
				width     : REAL;
				basis     : INTEGER;
				thickness : REAL);
```

```python
def vs.SetMarkerValue(dialogID, itemID, style, angle, length, width, basis, thickness):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the dialog|
|itemID|LONGINT|ID of the marker popup control|
|style|INTEGER|Marker Style|
|angle|INTEGER|Marker Angle|
|length|REAL|Marker Length (In Inches)|
|width|REAL|Marker Width (In Inches)|
|basis|INTEGER|Marker Thickness Basis|
|thickness|REAL|Marker Thickness|

## Examples
#### VectorScript ####
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
#### Python ####
```python

```

## See Also
VS Functions:
[GetMarkerValue](GetMarkerValue.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
