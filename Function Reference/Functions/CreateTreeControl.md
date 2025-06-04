# CreateTreeControl

## Description
Creates a Layout Manager tree control.

```pascal
PROCEDURE CreateTreeControl(
				nDialogID      : LONGINT;
				nComponentID   : LONGINT;
				nWidthInChars  : INTEGER;
				nHeightInChars : INTEGER);
```

```python
def vs.CreateTreeControl(nDialogID, nComponentID, nWidthInChars, nHeightInChars):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nWidthInChars|INTEGER|   |
|nHeightInChars|INTEGER|   |

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
dialog1 :INTEGER;
result  :INTEGER;
widthInChars, heightInChars :INTEGER;
root1, root2, child1, child2 :INTEGER;

PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
CASE item OF
SetupDialogC:
BEGIN
root1 := InsertTreeControlItem(dialog1, 4, 'root1', -1, 0);
child1 := InsertTreeControlItem(dialog1, 4, 'child1', root1, 0);
child2 := InsertTreeControlItem(dialog1, 4, 'child2', root1, child1);
root2 := InsertTreeControlItem(dialog1, 4, 'root2', -1, root1);
child1 := InsertTreeControlItem(dialog1, 4, 'child1', root2, 0);
child2 := InsertTreeControlItem(dialog1, 4, 'child2', root2, child1);
END;
END;
END;

BEGIN
dialog1 := CreateLayout('Example Dialog', FALSE, 'OK', 'Cancel');
widthInChars := 28;
heightInChars := 8;
CreateTreeControl(dialog1, 4, widthInChars, heightInChars);
SetFirstLayoutItem(dialog1, 4);
result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```
==== Python ====
```python
def Dialog_Handler(item , data ):
	SetupDialogC = 12255
	if item == SetupDialogC:
		root1  = vs.InsertTreeControlItem(dialog1, 4, 'root1', -1, 0);
		child1 = vs.InsertTreeControlItem(dialog1, 4, 'child1', root1, 0);
		child2 = vs.InsertTreeControlItem(dialog1, 4, 'child2', root1, child1);
		root2  = vs.InsertTreeControlItem(dialog1, 4, 'root2', -1, root1);
		child1 = vs.InsertTreeControlItem(dialog1, 4, 'child1', root2, 0);
		child2 = vs.InsertTreeControlItem(dialog1, 4, 'child2', root2, child1);


def Example():
	global dialog1
	dialog1 = vs.CreateLayout('Example Dialog', False, 'OK', 'Cancel')
	widthInChars = 28
	heightInChars = 8
	vs.CreateTreeControl(dialog1, 4, widthInChars, heightInChars)
	vs.SetFirstLayoutItem(dialog1, 4)
	result = vs.RunLayoutDialog(dialog1, Dialog_Handler)


dialog1 = 0
Example()
```

## See Also
VS Functions:
[GetTreeControlSelectedItem](GetTreeControlSelectedItem.md) 
| [InsertTreeControlItem](InsertTreeControlItem.md) 
| [RemoveTreeControlItem](RemoveTreeControlItem.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
