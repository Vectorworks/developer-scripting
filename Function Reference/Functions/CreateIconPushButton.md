# CreateIconPushButton

## Description
<b>[[VS:Vectorworks 2012 Deprecated Functions|DEPRECATED after Vectorworks2012]]</b>. See [[VS:AddButtonMode|AddButtonMode]] or [[VS:CreateImagePushButton|CreateImagePushButton]] for a replacement.

Creates an icon push button with the specified icon ID and width in characters.

```pascal
PROCEDURE CreateIconPushButton(
				nDialogID     : LONGINT;
				nComponentID  : LONGINT;
				nIconID       : INTEGER;
				nWidthInChars : INTEGER);
```

```python
def vs.CreateIconPushButton(nDialogID, nComponentID, nIconID, nWidthInChars):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nIconID|INTEGER|the index of the ICN# resource in the currently open rsrc file (or qtr on Windows)|
|nWidthInChars|INTEGER|   |

## Remarks
([[User:CBM-c-|_c_]], 2014.09.17): 
The routine still works under VW 2014, but not in VW 2015.

([[User:CBM-c-|_c_]], 2007.04.09): 
This routine is not recognized under VW 12.5 Fundamentals (might be VW 12.5.1)

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
dialog1 :INTEGER;
result  :INTEGER;
boo     :BOOLEAN;

PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
END;

BEGIN
boo := SetVSResourceFile('IP Resources');
dialog1 := CreateLayout('Example Dialog', FALSE, 'OK', 'Cancel');
CreateIconPushButton(dialog1, 4, 11021, 20);
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
	boo = vs.SetVSResourceFile('IP Resources')
	dialog1 = vs.CreateLayout('Example Dialog', False, 'OK', 'Cancel')
	vs.CreateIconPushButton(dialog1, 4, 11021, 20)
	vs.SetFirstLayoutItem(dialog1, 4)
	result = vs.RunLayoutDialog(dialog1, Dialog_Handler)
Example()
```

## Version
Availability: from VectorWorks 12.5
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
