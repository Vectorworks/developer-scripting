# GetMarkerChoice

## Description
<b>OBSOLETE procedure for VW2008</b>
Get current choice for Marker popup dialog control.

```pascal
PROCEDURE GetMarkerChoice(
				dialogID  : LONGINT;
				itemID    : LONGINT;
				VAR index : INTEGER;
				VAR style : INTEGER;
				VAR angle : INTEGER;
				VAR size  : REAL);
```

```python
def vs.GetMarkerChoice(dialogID, itemID):
    return (index, style, angle, size)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |
|index|INTEGER|   |
|style|INTEGER|   |
|angle|INTEGER|   |
|size|REAL|   |

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
int, dialogID   :INTEGER;
index, style, angle :INTEGER;
size :REAL;

PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
CASE item OF
SetupDialogC:
BEGIN
index := 1;
style := 2;
angle := 3;
size  := .125;
SetMarkerChoice(dialogID, 4, index, style, angle, size);
END;
5: 
BEGIN
GetMarkerChoice(dialogID, 4, index, style, angle, size);
AlrtDialog(Concat(
'index: ', index, Chr(13), 
'style: ', style, Chr(13), 
'angle: ', angle, Chr(13), 
'size: ', size));
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
def Dialog_Handler( item , data ):	
	if item ==	SetupDialogC:
		index = 1
		style = 2
		angle = 3
		size  = .125
		vs.SetMarkerChoice(dialogID, 4, index, style, angle, size)
	elif item == 5: 		
		vs.GetMarkerChoice(dialogID, 4, index, style, angle, size)
		vs.AlrtDialog(vs.Concat(
		'index: ', index, vs.Chr(13), 
		'style: ', style, vs.Chr(13), 
		'angle: ', angle, vs.Chr(13), 
		'size: ', size))


def Example():
	global dialogID
	global SetupDialogC
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
* [SetMarkerChoice](SetMarkerChoice.md) 
* [GetMarkerValue](GetMarkerValue.md)

## Version
GetMarkerChoice is obsolete as of VectorWorks 13.0

Availability: from VectorWorks 12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
