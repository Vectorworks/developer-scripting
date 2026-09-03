# SetRightItem

## Description
Places the specified control item to the right of a previously inserted control item.
Additional positioning can be performed by specifying x- and y-offsets (in pixels) from the initial insert position.

```pascal
PROCEDURE SetRightItem(
				dialogID    : LONGINT;
				srcItemID   : LONGINT;
				rightItemID : LONGINT;
				indent      : INTEGER;
				lineSpacing : INTEGER);
```

```python
def vs.SetRightItem(dialogID, srcItemID, rightItemID, indent, lineSpacing):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout being defined.|
|srcItemID|LONGINT|The index of the anchor control item.|
|rightItemID|LONGINT|The index of the control item being placed.|
|indent|INTEGER|Left-right (x) control offset value.|
|lineSpacing|INTEGER|Up-down (y) control offset value.|

## Remarks
Use the indent and lineSpacing sparingly.[DWD 1/20/00]

## Examples
```pascal
{* Position dialog control items *}
SetFirstLayoutItem (dialogID, 3);
SetRightItem (dialogID, 3, 4, 0, 0);
SetBelowItem (dialogID, 3, 5, 0, 0);
SetRightItem (dialogID, 5, 6, 0, 0);
SetBelowItem (dialogID, 5, 7, 0, 0);
SetBelowItem (dialogID, 7, 8, 3, -2);

{* Position dialog control items *}
	SetFirstLayoutItem (dialogID, 3);
	SetFirstGroupItem (dialogID, 3, 4);
	SetBelowItem (dialogID, 4, 5, 0, 2);
	SetRightItem (dialogID, 4, 6, 0, 0);
	SetRightItem (dialogID, 5, 7, 0, 0);

SetRightItem (dialogID, 5, 6, 0, 0);
SetRightItem (dialogID, 7, 8, 0, 0);
```
```python
import vs

# Places the specified control item to the right of a previously inserted
# control item.
dialogID = 1
srcItemID = 2
rightItemID = 3
indent = 10
lineSpacing = 1

vs.SetRightItem(dialogID, srcItemID, rightItemID, indent, lineSpacing)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
