# AddListBoxTabStop

## Description
Adds a tab stop to a Layout Manager list box.  The last parameter is the tab stop, in characters.  This function should be called in the dialog handler, as opposed to the dialog definition procedure.  This function will clear all data in the list control.

```pascal
PROCEDURE AddListBoxTabStop(
				dialogID : LONGINT;
				itemID   : LONGINT;
				tabStop  : INTEGER);
```

```python
def vs.AddListBoxTabStop(dialogID, itemID, tabStop):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the dialog|
|itemID|LONGINT|ID of the list box|
|tabStop|INTEGER|The tab stop, in characters|

## Remarks
The last parameter is the tab stop, in characters.  This function should be called in the dialog handler, as opposed to the dialog definition procedure.  This function will clear all data in the list control.

To insert choices into a list box that has tab stops, add tabs to the string to separate the values.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR

    dialog1 :INTEGER;
    result  :INTEGER;

    PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
    BEGIN
        CASE item OF
            SetupDialogC:
            BEGIN
    
                AddListBoxTabStop( dialog1, 4, 10 );
                AddChoice( dialog1, 4, concat( 'choice A', chr(9), 'A2' ), 0 );
                AddChoice( dialog1, 4, concat( 'choice B', chr(9), 'B2' ), 0 );
                AddChoice( dialog1, 4, concat( 'choice C', chr(9), 'C2' ), 0 );
                AddChoice( dialog1, 4, concat( 'choice D', chr(9), 'D2' ), 0 );
                AddChoice( dialog1, 4, concat( 'choice E', chr(9), 'E2' ), 0 );
                
            END;

            4:
            BEGIN
                AlrtDialog( 'selected' );
            END;
        END;
    END;

BEGIN

    dialog1 := CreateLayout( 'CreateListBox', FALSE, 'OK', 'Cancel' );

    CreateListBox( dialog1, 4, 30, 10 );
    
    SetFirstLayoutItem( dialog1, 4 );

    result := RunLayoutDialog(dialog1, Dialog_Handler);

END;

RUN(Example);
```
#### Python ####
```python
def Dialog_Handler(item, data):
	if item == SetupDialogC:
		vs.AddListBoxTabStop( dialog1, 4, 10 );
		vs.AddChoice( dialog1, 4, vs.Concat( 'choice A', vs.Chr(9), 'A2' ), 0 );
		vs.AddChoice( dialog1, 4, vs.Concat( 'choice B', vs.Chr(9), 'B2' ), 0 );
		vs.AddChoice( dialog1, 4, vs.Concat( 'choice C', vs.Chr(9), 'C2' ), 0 );
		vs.AddChoice( dialog1, 4, vs.Concat( 'choice D', vs.Chr(9), 'D2' ), 0 );
		vs.AddChoice( dialog1, 4, vs.Concat( 'choice E', vs.Chr(9), 'E2' ), 0 );
	elif item == 4:
		vs.AlrtDialog( 'selected' );

def Example():
	global dialog1, result, SetupDialogC
	SetupDialogC = 12255
	dialog1 = vs.CreateLayout( 'CreateListBox', 0, 'OK', 'Cancel' );
	vs.CreateListBox( dialog1, 4, 30, 10 );  
	vs.SetFirstLayoutItem( dialog1, 4 );
	result = vs.RunLayoutDialog(dialog1, Dialog_Handler);

Example()
```

## See Also
VS Functions:
[RemoveListBoxTabStop](RemoveListBoxTabStop.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
