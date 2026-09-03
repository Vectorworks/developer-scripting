# CreateEditInteger

## Description
Creates an editable text field control for INTEGER and LONGINT values.

CreateEditInteger is intended specifically for entry of numeric values; the control returns values in a numeric format, and supports calculations within the control field.

```pascal
PROCEDURE CreateEditInteger(
				dialogID          : LONGINT;
				itemID            : LONGINT;
				defaultValue      : LONGINT;
				widthInCharacters : LONGINT);
```

```python
def vs.CreateEditInteger(dialogID, itemID, defaultValue, widthInCharacters):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|defaultValue|LONGINT|Default value for the field.|
|widthInCharacters|LONGINT|Width of the field in characters.|

## Remarks
Edits long ints, does math,  get and set values with get and set integer calls

## Examples
#### VectorScript ####
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
CreateEditInteger(dialog1, 4, 123, 16);
SetFirstLayoutItem(dialog1, 4);
result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```
#### Python ####
```python
def Dialog_Handler( item , data):
	pass

def Example():
	dialog1 = vs.CreateLayout('Example Dialog', False, 'OK', 'Cancel')
	vs.CreateEditInteger(dialog1, 4, 123, 16)
	vs.SetFirstLayoutItem(dialog1, 4)
	result = vs.RunLayoutDialog(dialog1, Dialog_Handler)
Example()
```

```pascal
dialogID := CreateLayout(GetPlugInString(3001),TRUE,GetPlugInString(3002),GetPlugInString(3003));
CreateStaticText(dialogID,5,GetPlugInString(3004),-1);
CreateStaticText(dialogID,6,GetPlugInString(3005),-1);
CreateStaticText(dialogID,7,GetPlugInString(3006),-1);
CreateEditInteger(dialogID,8,0,6);
CreateEditInteger(dialogID,9,0,6);
CreateEditReal(dialogID,10,3,0.0,6);
{ select the result type controls. }
CreateStaticText(dialogID, kSelResTypeStaticTxt, GetPlugInString(3018), -1);

CreateGroupBox( dlgId, kSettingsPanel,'', False );{kSettingsPanel}
CreateStaticText( dlgId, kHeightLabel, GetPluginString(3019), -1 );{kHeightLabel}
CreateEditReal( dlgId, kHeightEdit, 1, 0.0, 20 );
CreateStaticText( dlgId, kFloorCountLabel, GetPluginString(3020), -1 );
CreateEditInteger( dlgId, kFloorCountEdit, 0, 20 );
CreateCheckBox( dlgId, kAllowIndividualCheck, GetPluginString(3021) );
CreateCheckBox( dlgId, kSetSlabCheck, GetPluginString(3022) );
CreateStaticText( dlgId, kSlabThicknessLabel, GetPluginString(3023), -1 );
CreateEditReal( dlgId, kSlabThicknessEdit, 1, 0.0, 20 );

BEGIN
CreateStaticText(dialogID, ndx2DlogID1(cnt), Concat(flds[cnt].locName, ':'), -1);
CreateEditInteger(dialogID, ndx2DlogID2(cnt), 10, fldWidth);
END;
```
```python
import vs

# Creates an editable text field control for INTEGER and LONGINT values.
dialogID = 1
itemID = 2
defaultValue = 3
widthInCharacters = 10

vs.CreateEditInteger(dialogID, itemID, defaultValue, widthInCharacters)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
