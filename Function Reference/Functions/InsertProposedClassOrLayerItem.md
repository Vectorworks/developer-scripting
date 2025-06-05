# InsertProposedClassOrLayerItem

## Description
<b>[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)</b>.  See [[VS:InsertPropClassOrLayerItem|InsertPropClassOrLayerItem]] for a replacement.

Inserts a class or layer item in the proposed section of a Class, Design Layer, or Sheet Layer Layout Manager Pull Down.

```pascal
FUNCTION InsertProposedClassOrLayerItem(
				nDialogID    : LONGINT;
				nComponentID : LONGINT;
				strLabel     : STRING;
				nIconIndex   : INTEGER): BOOLEAN;
```

```python
def vs.InsertProposedClassOrLayerItem(nDialogID, nComponentID, strLabel, nIconIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|strLabel|STRING|   |
|nIconIndex|INTEGER|   |

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
dialog1 :INTEGER;
result  :INTEGER;
boo     :BOOLEAN;
choiceNumber :INTEGER;
choiceString :STRING;

PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
CASE item OF
SetupDialogC:
BEGIN
boo := InsertProposedClassOrLayerItem(dialog1, 4, 'New Class Name', 0);
END;
1:
BEGIN
GetSelChoice(4, 0, choiceNumber, choiceString);
AlrtDialog(Concat('choiceString: ', choiceString));
END;
END;
END;

BEGIN
dialog1 := CreateLayout('Example Dialog', FALSE, 'OK', 'Cancel');
CreateClassPullDownMenu(dialog1, 4, 24);
SetFirstLayoutItem(dialog1, 4);
result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks13.0
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
