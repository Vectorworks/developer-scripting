# CreateMarkerPopup

## Description
Creates a popup control that displays the various marker styles available in VectorWorks and allows the user to choose one.  Markers are the adornments at the endpoints of line objects and consist of styles like arrow, circle, cross, etc.

```pascal
PROCEDURE CreateMarkerPopup(
				dialogID    : LONGINT;
				componentID : LONGINT);
```

```python
def vs.CreateMarkerPopup(dialogID, componentID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Id of the dialog|
|componentID|LONGINT|Id of the popup control|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
dialog1	:INTEGER;
result	:INTEGER;

PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
END;

BEGIN
dialog1 := CreateLayout('Untitled Dialog', FALSE, 'OK', 'Cancel');
CreateMarkerPopup(dialog1, 4);
SetFirstLayoutItem(dialog1,  4);
result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```
#### Python ####
```python
def Dialog_Handler( item , data ):
	pass

def Example():
	dialog1 = vs.CreateLayout('Untitled Dialog', False, 'OK', 'Cancel')
	vs.CreateMarkerPopup(dialog1, 4)
	vs.SetFirstLayoutItem(dialog1,  4)
	result = vs.RunLayoutDialog(dialog1, Dialog_Handler)

Example()
```

## Version
Availability: from VectorWorks10.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
